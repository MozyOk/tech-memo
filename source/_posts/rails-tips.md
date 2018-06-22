---
title: rails-tips
date: 2018-06-23 01:53:09
tags: rails
---

Procfileを使っていても RAILS_ENV=production のようなオプションは使える
===

Procfile
```s
web: bundle exec rails s -p 3000
```

terminal
```s
$ make run RAILS_ENV=production
```

production のみ非表示にするときのベスト?なプラクティス
===

```ruby
# こっちがいいかも
def new
  raise ActionController::RoutingError, "NOT FOUND" if Rails.env.production?
  super
end
```