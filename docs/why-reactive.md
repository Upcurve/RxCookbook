# The Why
Now that we have had a brief about what ReactiveX is and how this guide is supposed to help you, it's time we get into the purpose of using ReactiveX in the first place.
 
## What is Reactive Programming?
If you've ever written any event based program then you're at least indirectly tasted a flavour of reactive programming.

If you want a formal definition, here's what **Wikipedia** has to say:

> In [computing](https://en.wikipedia.org/wiki/Computing), reactive programming is a declarative [programming paradigm](https://en.wikipedia.org/wiki/Programming_paradigm) concerned with [data streams](https://en.wikipedia.org/wiki/Dataflow_programming) and the propagation of change.

In simple terms, in reactive programming, you declare some actions or rules and the program follows accordingly. Reactive programming is _asynchronous_.

Let's clear up the haze with a straightforward example.

Imagine a simple button click on an app in your smartphone. Your requirement here is to do an action on the button click and also to make sure that unnecessary rapid clicks are prevented.

How do you do that?

Do you keep a count? Or do you disable the button after the first click until a given period of time has elapsed?

Well, if you think _imperatively_, that's what you need to do. Reactive is much simpler and causes less headaches.

In reactive programming you can treat each button click as an event or an emission and allow only the first or last emission in a given time window say **1 second** to be considered as valid. Once you've declared this rule, you're done. Pack your bags, go home and browse Netflix.

## Why choose Reactive Programming?
If you think about our world, everything you do is a reaction to some event.

You switch on the lights because it's dark and you cannot see. You hit the brakes on your car because you see a roadblock ahead.

We _react_.

If we are to model softwares that fit into our world, they need to be reactive as well. Apps need to be responsive, _instantaneous_.

No one likes a sluggish app. There's no room for waiting for one task to finish and then start another. Parallel processing is at the heart of modern softwares.

To be more responsive, apps need to be more reactive. They need to react instantly to our actions or rather events without waiting for anything.

If your tweets have finished loading then they need to show up on the screen. If your phone's battery is about to die then it should give you an indication.

Without these traits, it's hard or rather impossible to create modern softwares that fulfills our needs.

## How can ReactiveX help?
**ReactiveX** or **Reactive Extensions** as you might call them, are a bunch of tools that make your job easy in modelling your apps in a reactive fashion and handling asynchronous data streams.

Be it a simple button click like the previous example, or some complex data, these extensions can help you get your job done without dealing with the complexities behind them.

However, as the saying goes, a tool is only as powerful as you can harness it.

Knowing which extensions to use in a particular scenario is the biggest challenge. That is where this cookbook comes to play.

With real-world examples, you'll start to think everything in a reactive fashion, making it easy to work with ReactiveX and get your code rolling.

### Visible benefits of using ReactiveX
* Codebase becomes smaller and cleaner
* Less time is spent in solving common yet complex issues
* Concurrency becomes a piece of cake
* No more intricate program state handling

## Where can ReactiveX be used?
ReactiveX came out as a concept and has been implemented in most major languages available today.

The list includes some of the veterans and the newbies:

* Java
* Swift
* Kotlin
* C++
* Clojure
* Javascript
* Python
* PHP
* Go
* Ruby
* Dart
* Groovy

... and it goes on.

In short, you're pretty much covered.

ReactiveX is everywhere, making them even more beneficial to learn and start using them right away.