---

layout: post

title: groovy basic 

date: 2018-05-10 15:54:45 -0800

description: 

tags: [groovy]

---

#Groovy

##Closures

###Parameters

```groovy
def power = { int x, int y -\>
 return Math.pow(x, y)
}
```

####you can also skip the type of parameters
```groovy
def say = { what -\>
 println what
}
```
####closure can accept one parameter which is available by the name it inside of the closure
```groovy
def say = { println it }
```
###Optional Return

the last statement of a method block (or closure) is returned implicitly

###Passing Closures around
```groovy
def transform = { str, transformation ->
 transformation(str)
}
println transform("Hello World", { it.toUpperCase() })
``` 


###Closing of variables
```groovy
def createGreeter = { name -\>
 return {
 def day = new Date().getDay()
 if (day == 0 || day == 6) {
 println "Nice Weekend, $name"
 } else {
 println "Hello, $name"
 }
 }
}

def greetWorld = createGreeter("World")

greetWorld()
```

##Implicit Truthy

- Strings: If empty false, otherwise true
- Collections and Maps are true if they are not empty
- All non-zero numbers are true
- Matchers (from a regular expression check) are true if they found at least one match
- Iterators with further elements are true
- Object references are true if they aren't null (you can define a custom truthy logic for your classes by implementing the boolean asBoolean() method)

##New and noteworthy Operators

Safe Navigation Operator “?”
```groovy
if(company.getContact()?.getAddress()?.getCountry() == Country.NEW\_ZEALAND) { ... }
```
##Ranges

- 1..10 - an inclusive Range
- 1..\<10 - f an exclusive Range
- ‘a’..’x’ – Ranges can also consist of characters
- 10..1 – Ranges can also be in descending order
- ‘x’..’a’ – Ranges can also consist of characters and be in descending order.

##Regular Expressions

def matcher = "The Hitchhiker's Guide to the Galaxy" =~ /Galaxy/

```groovy
if (matcher) {
 println "Found the word 'Galaxy'"
}
```

if You define a string inside two slashes /../, that you don't need to escape a backslash character,

##Traits 

They can be seen as interfaces carrying both default implementations and state.

- Traits may implement interfaces
- A trait may define properties
- Traits may extend another trait, using the extends keyword.