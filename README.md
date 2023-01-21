# Contents
- TODO

# introduction 

this is a guide for learning JavaScript decorators feature deeply. we will cover basics and also advanced topics of decorators, and will review various examples for mastering it. TODO: improve grammer

this is a detailed and long guide, and it's for those developers who want to have a good undrestanding with full details on this topic, so if you want to just have a basic undrestanding of decorators to get started with it maybe you dont need this tutorial since it is very detailed and will discuss advanced topics that you may never have on realworld scenarios, but surely this guide will help you to have master the decorators on javascript. TODO: improve grammer

# what is decorator 
typescript are some functions in javascript that can be attached to a class or its members like methods or properties to change their behaviour. decorator functions will receive some specific arguments which help us to have some details about the things that are attached to and with this details we can control, track or modifying the behaviour of their attached thing :TODO: find something else instead of thing + improve grammer 

TODO: add more details here + compare with other languages decorations or annotations
TODO: check if decorators are builtin implementation for decorator design pattern and according to that say more details of difference between it and decorator design pattern


# getting started 
this is a basic example of decorator usage in typescript 

```JAVASCRIPT
@MyDecorator
class Car {
  // class implementation
}
```

in the above example `@MyDecorator` is the way that we are using our decorator, decorator name is `MyDecorator` and we are using it with a `@` prefix and placed it before the class name, we will see the syntax and usage in detail and this is just a simple example to become familier with the Decorator

in this example we just showed the usage and not the way that we can define the decorator because the one of the most important reasons that we use decorators is that they are realy easy to use and have a clean syntax

decorators are in the stage 2 of Ecma porpusals, that mean they are not available in native javascript in browser or node by default, and also they are not stable and their API may change in feature, but surely their changes wouldn't be alot. you can use decorators with transpile tools like babel or Typescript. this is the reason that we wrote the above example ( and other examples in this guide ) in TypeScript. 

note that even typescript and babel dont support decorators by default and there should be some extra configurations to be able to use it on them. if you want to see a full guide of how you can get started with decorators in Typescript or Babel code you can refrence to their section and see a full guide for getting started.

some realworld examples which decorators can become handy: 

- TODO: list examples with details 

also we would have some examples in this guide that are very similar to realworld issues that can be resolved easily with decorators

# decorators are wrapper functions with metaprogramming abilities 

but why we need to use decorators? if typescript and babel can convert our code with decorators to native javascript doesn't mean that we can wrote some code without decorators that is totally equvalent with the code with decorator but just with different syntax?

the answer is yes, we can live without decorators as we did till now and also can simulate their behaviour completely in native javascript without. but with decorators it will be very cleaner and without redandant code. exaclty like classes that are a suger syntax to hide those nasty and dirty codes that we had to wrote in native JavaScript to have class like behaviour and creating prototype chained objects. 

you can think of decorators as a suger syntax ( not exactly ) for wrapper functions that also gives you some metaprogramming abilities. but what are wrapper functions and metaprogramming? we will explain those in next sections.

# what is a wrapper function 

# what is metta programming 

# decorator types ( class , method .... ) 

# class decorator 

## how to use class decoraotr 
- mention why we are showing the way of using first 

## how to define class decorator function 

## using a factory 

## when we use it for abstract classes 

## what we can do with it ? 

## example for using a list of all classes 

## example for changing class members and statics 

## list other examples ( titles only ) 

# method decorators 

#  in order -> 

- how to use, 
- define, 
- why we get prototype instead of the class itself,  
- using factory, 
- when on static methods , 
- private methods 
- prottected methods 
- on abstract methods ( can we ? ), 
- what we can do with it 


## diff for implementation and usage with class decorators 

## can we just use class decorators instead ? 

## when we should use class decorator instead of method decorator 

## which one will be executed first class or method decorator ? 

## example with controller router 

## other examples 

# properties 

## for properties the same items + : 

- why we dont have value on decoration for properties 
- why its different from method, they are both properties right ? 

# ... other type of decorators 

#  how it would be compiled in ts 
# how it would be compiled in babel 
# what is the current status ? 

