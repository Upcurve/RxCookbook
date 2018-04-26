# Introduction

Welcome to The ReactiveX Cookbook. This guide is designed to help you grip the concepts of Reactive Extensions or ReactiveX or Rx in an easy and effective way.

## What is ReactiveX?

**ReactiveX** is a library aimed at helping you write asynchronous programs using the `Observer` pattern. The main strength of **Rx** lies in it's arsenal of powerful operators.

To give you a taste of what Rx operators can do, here's a piece of code:


```kotlin
Observable.just(1,2,3,4)
    .filter { it > 2 }
    .map { it * 10 }
    .subscribe { println("Now Showing: $it") }

```

With these **4 lines** of **Kotlin** code you can do a quick filtering from your data source and transform the filtered values by multiplying each emitted number by **10**.

This was just a sneak peek. More is about to come.

ReactiveX is not tied to a specific language, you can have ReactiveX for most of the popular languages like Java, Kotlin, Swift, Python, etc.

## What to expect from this guide?

This guide will provide you with real world examples of how you can incorporate the reactive approach into your applications.

You will see code samples that will help you get started in no time.

Although this guide will mainly focus on applying **Rx** to mobile apps *(Android & iOS)*, once you get a clear understanding of how **Rx** works, you should be able to apply the concepts everywhere.

## Prerequisites

Following this guide requires you to have a basic understanding of:

- **Android** or **iOS** app development
- ​[**Kotlin**](https://kotlinlang.org/) or [**Swift**](https://developer.apple.com/swift/)​

## How to get the most out of this guide?

While reading is good, reading and then application of the gained knowledge is so much better. That is why it's a great idea to have your **IDE** opened at all time when you go through this guide.

As soon as you're done with a new concept, try out some of the snippets given in the page. Experiment by modifying the supplied snippets and see how they behave.

This approach will help you understand the topics better and will also help you remember the various operators and when and where to actually use them.

*Happy coding!*
