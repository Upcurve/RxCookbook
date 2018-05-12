# Creating Observables

Creating your own `Observable` isn't rocket science. It's fairly simple thanks to all the helper functions provided by **ReactiveX**. In this chapter we'll be exploring multiple ways to create an `Observable` to serve your needs.

ReactiveX offers a list of helper functions to create your own `Observable` from a data source. Here are the most _common_ ones:
* `just()`
* `from()`
* `create()`
* `defer()`
* `range()`
* `interval()`

## Emitting single value
If you have a value that you need to convert into an emission of an `Observable` then you need the `just()` function to do your job.

#### Android

```kotlin
Observable.just("Groot")
        .subscribe { println("I'm $it") }
```

#### iOS
```swift
Observable.just("Groot")
        .subscribe { print("I'm $0") }
```

#### Web
```javascript
Rx.Observable.just("Groot")
        .subscribe(val => console.log("I'm ", val))
```

## Emitting a sequence of values
When you need to emit multiple values in _sequence_, you need the `from()` function.

If you have a list, you can just supply that list to `from()` and it will emit each item one by one.

#### Android
```kotlin
Observable.fromIterable(mutableListOf(1, 2, 3, 4, 5))
        .subscribe { println("Currently Serving: Order No - $it") }
```

#### iOS
```swift
Observable.from([1, 2, 3, 4, 5])
        .subscribe { print("Currently Serving: Order No - $0") }
```

#### Web
```javascript
Rx.Observable.from([1, 2, 3, 4, 5])
        .subscribe(val => console.log("Currently Serving: Order No -", val))
```

## Emitting based on custom logic
When you need to apply your custom logic to create an `Observable` you need to resort to the `create()` function.

This is helpful when you have a stream of data such as button clicks, location events, etc. and you want to convert them to an `Observable`.

You just need to have **3** things on your mind:
* Emit each value by calling the `onNext()` function
* Mark the end of emissions by calling the `onComplete()` function
* Call the `onError()` function in case of any error or exception

#### Android
```kotlin
Observable.create<String> {
    if (!it.isDisposed) {
        it.onNext("We")
        it.onNext("<3")
        it.onNext("Upcurve")
        it.onComplete()
    }
}.subscribe { print("$it ") }
```

## Emitting a range of values
There might be some cases where you need to emit a range of values, let's say **1** to **100**.

Although this can be done by supplying a list to `from()` or creating your own `Observable` by using `create()` but there's a better way.

**Rx** calls it the `range()` function. You can easily generate a range by supplying the start value and the no of values to emit.

#### Android
```kotlin
Observable.range(1, 100)
        .subscribe { println(it) }
```

## Emitting values at a given interval
What about when you need a sort of timer?

Rx has a solution to that as well. Behold the `interval()` function. With this function you can specify a time interval and the `Observable` will emit a `Long` value at each interval.

This kind of `Observable` is helpful when you combine it will another `Observable` to emit values or do something after every let's say **N** seconds.

Another very common use case for this function is **polling**.

#### Android
```kotlin
Observable.interval(5, TimeUnit.SECONDS)
        .subscribe { println("Hi, there!") }
```