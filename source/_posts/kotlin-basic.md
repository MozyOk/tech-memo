---
title: kotlin-basic
date: 2018-06-22 00:10:22
tags: kotlin
---

kotlin var val 比較
===

```kotlin
var fish = 50
val dog = 50
fish == dog
>>true
```

when式とlengthの使い方
===

```kotlin
var welcomeMessage = "Hello and welcome to Kotlin"
when (welcomeMessage.length) {
   0 -> println("Nothing to say?")
   in 1..50 -> println("Perfect")
   else -> println("Too long!")
}
```

Array & loop
===

```kotlin
val array = Array(7){1000.0.pow(it)}
val sizes = arrayOf("byte", "kilobyte", "megabyte", "gigabyte", "terabyte", "petabyte", "exabyte")
for ((i, value) in array.withIndex()) {
   println("1 ${sizes[i]} = ${value.toLong()} bytes")
}
```