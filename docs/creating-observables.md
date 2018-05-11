# Creating Observables

Creating your own `Observable` isn't rocket science. It's fairly simple thanks to all the helper functions provided by **ReactiveX**. In this chapter we'll be exploring multiple ways to create an `Observable` to serve your needs.

ReactiveX offers a list of helper functions to create your own `Observable` from a data source. Here are the common ones:
* `just()`
* `from()`
* `create()`
* `defer()`
* `range()`
* `interval()`
* `empty()`
* `never()`
* `error()`

## Emitting single value
If you have a value that you need to convert into an emission of an `Observable` then you need the `just()` function to do your job.

### Android

```kotlin
Observable.just("Groot")
        .subscribe { println("I'm $it") }
```

### iOS
```swift
Observable.just("Groot")
        .subscribe { print("I'm $0") }
```

### Web
```javascript
Rx.Observable.just("Groot")
        .subscribe(val => console.log("I'm ", val))
```

## Emitting a sequence of values
When you need to emit multiple values in _sequence_, you need the `from()` function.

### Android
```kotlin
Observable.fromIterable(mutableListOf(1, 2, 3, 4, 5))
        .subscribe { println("Currently Serving: Order No - $it") }
```

### iOS
```swift
Observable.from([1, 2, 3, 4, 5])
        .subscribe { print("Currently Serving: Order No - $0") }
```

### Web
```javascript
Rx.Observable.just([1, 2, 3, 4, 5])
        .subscribe(val => console.log("Currently Serving: Order No -", val))
```