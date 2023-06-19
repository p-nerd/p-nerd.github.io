---
title: কোটলিনের পরিচয়
publishDate: 2022-10-15 00:00:00
img: /assets/blogs/kotlin.png
img_alt: Java Virtual Machines-এর জন্য একটি আধুনিক প্রোগ্রামিং ভাষা| Better Java
description: |
    Java Virtual Machines-এর জন্য একটি আধুনিক প্রোগ্রামিং ভাষা| Better Java
tags:
    - JVM
    - kotlin
    - Programming
---

কটলিন (Kotlin) একটি স্ট্যাটিকালি টাইপ করা মাল্টি-প্যারাডাইম প্রোগ্রামিং ল্যাঙ্গুয়েজ যা জাভা-এর একটি ভাল বিকল্প হিসাবে ডিজাইন করা হয়েছে।
জাভার মতো এটি জাভা ভার্চুয়াল মেশিনে চালিত বাইটকোডগুলিতে কম্পাইল করে, তবে কোটলিন আধুনিক ডেভেলপারদের পছন্দের আরও সংক্ষিপ্ত সিনট্যাক্স এবং ল্যাঙ্গুয়েজ ফিচার সরবরাহ করে। যেমন: টাইপ ইনফারেন্স, ফাংশনাল প্যার্টান, নাল সেফটি এবং আরও অনেক কিছু। এটি 2011 সালে Jetbrains দ্বারা ঘোষণা করা হয়েছিল এবং 2016 সালে এর প্রথম স্ট্যাবল ভার্শন প্রকাশ করা হয়।

এটি রাশিয়ার Kotlin দ্বীপের নামে নামকরণ করা হয়েছে। এর মূল বৈশিষ্ট্যগুলির মধ্যে একটি হল এটি বিদ্যমান জাভা কোডের সাথে ইন্টারপ করতে পারে যার অর্থ ডেভেলপারা তাদের সমস্ত জাভা কোড আবর্জনার মধ্যে না ফেলে ধীরে ধীরে এটি গ্রহণ করতে পারে। JVM ছাড়াও কটলিন নেটিভ কোড এবং জাভাস্ক্রিপ্টে কম্পাইল করে মাল্টি-প্ল্যাটফর্ম অ্যাপের দরজা খুলে দিতে পারে।

এটি অ্যান্ড্রয়েড ডেভেলপমেন্ট কমিউনিটিতে সবচেয়ে বেশি প্রভাবশালী এবং 2019 সালে গুগল জাভার পাশাপাশি কটলিনকে অ্যান্ড্রয়েড ডেভেলপমেন্টের জন্য পছন্দের ভাষা হিসেবে নির্ধারণ করেছে। এর কিলার বৈশিষ্ট্যগুলির মধ্যে একটি হল co-routines যা মোবাইল ডেভেলপারদের জন্য একটি সাধারণ প্রয়োজনীয়তা অ্যাসিঙ্ক্রোনাস নন-ব্লকিং কোড লেখার একটি সরলীকৃত উপায় প্রদান করে।

কটলিন কোড শুরু করার জন্য একটি ফাইল তৈরি করুন শেষ করুন .kt দিয়ে। অধিকাংশ কটলিন ডেভেলপাররা Intellij Idea মতো কিছু ব্যবহার করে। আবার Intellij Idea Jetbrains দ্বারাই তৈরি।

```kotlin
fun main() {
    var hello = "Hello World" // type inference
    var hello2: String = "Hello World 2" // explicit typing
    var hello3: String? = "Hello World 3" // nullable variable

    println(hello)
}
```

ফাইলের ভিতরে একটি main ফাংশন সংজ্ঞায়িত করতে "fun" কীওয়ার্ড ব্যবহার করুন। এখানেই আপনার কোড কার্যকর করা শুরু হবে এবং এই সিনট্যাক্সটি "public static void main string args" এর চেয়ে অনেক বেশি মজাদার।

"var" কীওয়ার্ড দিয়ে একটি ভেরিয়েবল ঘোষণা করুন, একটি মান বরাদ্দ করুন এবং এর ধরন স্বয়ংক্রিয়ভাবে অনুমান করা হবে type inference এর মাধ্যেমে অথবা আপনি explicit type জন্য এর variable এর নামের পর কোলন যোগ করে টাইপ নির্ধারণ করতে পারেন।
একটি ভেরিয়েবল null হতে পারে না যদি না আপনি এটিকে "?" দিয়ে স্পষ্টভাবে অনুমতি দেন। ভেরিয়েবলটিকে স্ট্যান্ডার্ড আউটপুটে লগ করতে println ব্যবহার করুন। লক্ষ্য করুন কিভাবে সেমিকোলন ঐচ্ছিক।

```kotlin
class Humanoid {
    // attribute
    var name = "Shihab"

    // method
    fun yoName() {
        print(name)
    }
}

// extension function
fun Humanoid.walk() {
    println("waling ...")
}
```

কটলিন পরিচিত object-oriented প্যার্টান সমর্থন করে কিন্তু এটি বিশেষ ফাংশনাল জিনিস করতে পারে যা জাভা পারে না।
যেমন: এক্সটেনশন ফাংশন ব্যবহার করে inheritance ছাড়াই একটি class এর আচরণ পরিবর্তন করতে পারে।

```kotlin
// first-class function
fun double(x: Int) = x * 2;

// anonymous lambda function
var lambda: (Int) -> Int = {num -> double(num)}

```

কটলিনে ফাংশন হল first-class-objects যার মানে এগুলি ভেরিয়েবল হিসাবে সংরক্ষণ করা যেতে পারে, আর্গুমেন্ট হিসাবে পাস করা যেতে পারে বা lambdas এর সাথে anonymously ব্যবহার করা যেতে পারে।

```kotlin
data class User(val name: String, val age: Int)

val person = User("shihab", 19);

val {name, age} = person;
```

কটলিন ডেটা ক্লাসের মতো জিনিসগুলি দিয়ে boilerplate কোড হ্রাস করে সাহায্য করে। যাতে আপনাকে কনস্ট্রাক্টর, গেটার এবং সেটার লিখতে না হয় এবং কোনও বস্তুর মানগুলি অ্যাক্সেস করার সময় destructuring সমর্থন করে, আপনাকে concise efficient কোড লেখার অনুমতি দেয়।

এখন আপনি টার্মিনালে এবং কটলিন কম্পাইলার চালিয়ে একটি জার ফাইলে কটলিন কােড কম্পাইল করতে পারেন। `kotlinc hello.kt -include-runtime -d hello.jar`

এখন কটলিনের feature গুলো পয়েন্টআউট করলে আমার দেখতে পাই।
Concise Syntax (Write less)
Null Safety
First-class-function expression
Interoperable with Java (We can use existing JVM library or framework)
Multiplatform:
Android
Server-side with JVM
Web frontend (Kotlin also compile to javascript)
Cross platform mobile applications

এটাই ছিল কটলিন নিয়ে একটা ব্যাসিক ভূমিকা। কটলিন নিয়ে আরো জানার জন্য ভিজিট করুন: https://kotlinlang.org/

ধন্যবাদ :)
