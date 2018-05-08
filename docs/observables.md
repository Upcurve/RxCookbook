# Understanding the Observer Pattern

ReactiveX is based on a design pattern called **The Observer Pattern**. This section is focused on explaining what this is and how to wrap your head around this concept.

The Observer Pattern works in two parts:
* Observable
* Observer

Let's use a real world example to understand the concepts more clearly.

## Imagine this

You're sitting in a room looking at me on a stage right in front of you. I'm walking to-and-fro on that stage explaining how **Rx** works.

Now let's break that imagination down to make more sense out of it.

## What is an Observable?
In the simplest of terms, an `Observable` is a source of continuous data. Taking the above imagination into consideration, I'm the `Observable` here.

By speaking continuously, I'm *emitting* data to be _observed_ by any `Observer`.

## Who are the Observers?
Just as any speaker would need an audience (_otherwise it kind of looks weird speaking in an empty hall_), an `Observable` needs at least one `Observer`.

Can you figure out who's the `Observer` in your imagination?

If you guessed it to be you, you're a genius. Listening to me speaking on the stage, you're playing the role of being the `Observer` here.

You're _observing_ whatever I'm _emitting_ at you.

## Data flow in the chain
In the **Observable-Observer** chain, data flows from the `Observable` to the `Observer`.

Coming back to our original scenario, since I'm the `Observable` and you're the `Observer`, data is flowing from me to you. In other words, words are flowing from my mouth to your ears.

This flow doesn't necessarily be a simple one. Data can pass through multiple **operators** and undergo and series of changes and filtering before they even reach the `Observer`.

## Tell me more about Operators
Operators in **ReactiveX** is very similar to those in mathematics. Operators take in data, perform some function on them and gives a changed data set as a result.

Let's another person to our original scenario - _a translator_.

Imagine that I'm delivering my speech in **English**. However, you can understand only **German**. How do you understand what I'm talking about?

Here's where the translator comes to play. The translator translates whatever I'm saying from **English** to **German** and relays the same to you as and when I speak.

In this case, the translator is the operator, translating English words to German before they reach you.

You can call operators as **middlemen**, packaging the incoming data in a way that is understandable to the observers.

We'll see plenty of operators in action throughout this book. Keep reading (_and refilling your cup of coffee_).

## Single or multiple Observers?
Very similar to the fact that there can be multiple people sitting in the hall listening to me speak, an `Observable` can have multiple observers.

Each `Observer` can in turn have their own chain of operators preceding their observation point.