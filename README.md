# Contents


# Decorator basics

in this section we will be introduced with decorators and see what it is and what it can do

## What is a decorator?

A decorator is a special kind of function in TypeScript that can be applied to a class, method, accessor (getter and setter), property, or parameter. It allows developers to add new behavior or modify the structure of the decorated element, such as adding additional functionality or changing how the element behaves. Decorators are invoked using a specific syntax and can be used for tasks such as logging, validation, or dependency injection. They allow developers to add new behavior to existing classes, methods and properties, without having to change the original code.

this is a deffination from [Typescript docs](https://www.typescriptlang.org/docs/handbook/decorators.html#decorators), but if its still hard for you to undrestand you are not alone. for better undrestanding you should know why you need to use decorators, what problem they solve and finally how they are implemented

this respository tries to explain decorators step by step in deep. first we review the basics of a decorator ( that isn't new ) and then try to dig deep into details to master it.

## defining a simple decorator

a decorator is nothing but a simple function : 

``` JAVASCRIPT

function MyFirstDecorator() {
  // do something
}
```
decorators are function, in this example we used function declaration but decorators are not have to be function declaration, they can be function expression like `const MyFunctionDecorator = function(){}` or even they can be an arrow function `const MyFunctionDecorator = () => {}`

so if decorator is just a function then any function can be a decorator right? 
typicly yes, all the functions can be a decorator. but decorators will receive specific arguments so when we have a decorator we should specify them. 

## using a decorator 

the way that we will use decorators is important, because the most important reason that we will use a decorator instead of a function is that its usage is very simple and makes our code prettier. 
if it wasn't then we could just use our normal functions and call them ( with special arguments ) instead of decorators right?
so you probably guess that their usage is so user friendly, or we can say that it has a good DX ( developer experience )

here is an example of how we can use the decorator that we defined in the previous section

```JAVASCRIPT
@MyFirstDecorator
class Car {
  // Car class defination  
}
```

we have a `@` symbol before the name of our decorator ( function ) and then we placed it before the class defination, this way of using it will make it a class decorator, because its before of a class. so you can guess when we use it for a class it will be applied on the class.

but if this is a class decorator usage is there any more usages? 
yes, as the defination from the first section explains we can apply a decorator to : 

- classes
- properties 
- methods
- parameters
- accessors (getters and setters)

lets review each usage 

## Class decorator

as privious example, we can apply a decorator to a class by simply placing it before the class defination.

```JAVASCRIPT
@MyFirstDecorator
class Car {
  // Car class defination  
}
```

now what we can do with it? the answer is what ever you can do with a class Object. for example you can set properties on it, change its prototype and etc. we will see some example usages for better undrestanding later in this guide

in our decorator function we will receive the constructor function ( the class itself ) as the first argument. this is our decorator implementation function from before, now we can define its parameter as below:

```TYPESCRIPT
function MyFirstDecorator(constructor: Function) {
  classObject === Car // true
  // do something else with the Cat class 
}
```

so the first argument of a decorator function is the constructor function ? not always.

when we apply decorator on a class the first argument will be the constructor but when we apply it on other stuff like properties or methods and etc we will receive different values for the first argument 

so the defination of a decorator function is based on its place of usage, if we use it as a class decorator it gonna recive the constructor function as the first argument but if we use it as a property decorator or method decorator, it will receive different value for the first argument ( that will se those later )

don't be worry we will summary all the available arguments for decorators later but for now just remember class decorators will receive classObject as the first argument 

note1: the class decorator function receives just one argument and that is the constructor function
note2: every class is actually a constructor function thats why we specified `Function` as the type of argument
note3: in above when we say constructor function we mean the `Cat` class itself


## property decorator 

now lets see an example of method decorator when a decorator is applied on method

```JAVASCRIPT
class Car {
  @MyFirstDecorator
  drive(){
    // method implementation
  }
}
```

method decorator is so similar, but it is placed before method instead of class 

what would be the method decorator arguments?

```
function MyFirstDecorator(prototype: any, propertyKey: string) {
  prototype === Cat.prototype // true
  propertyKey === 'drive' // true
  // do something else with the method
}
```


