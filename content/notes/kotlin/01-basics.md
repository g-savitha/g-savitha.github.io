---
title: "Kotlin basics"
date: 2021-10-17T14:17:40+05:30
draft: false
tags: [kotlin]
categories: [android, kotlin]
sources: [https://developer.android.com/]
---

<!--

::Annotation Guide::
~~~~~~~~~~~~~~~~~~~~

* `em` is the modifier

1. em (_text_) - blue underline
2. strong (**text**) - yelow highlight
3. del (~~text~~) - red strike-through

4. em > em (_*text*_) - blue circle
5. em > strong (_**text**_) - lawngreen box
6. em > del (_~~text~~_) - red cross-off
-->

1.  `fun` is a leyword used to define a function.

    ```kotlin
     fun main() {
         println("Happy Birthday!")
         println("Jhansi")
         println("You are 25!")
     }
    ```

2.  `print()` vs `println()`

    - `print()` just prints the text without using a line break at end of string.

3.  `val` keyword is used to store the values that _can be set only once_. same like `const` in js. For declaring a _changeable variable_ use `var`

    ```kotlin
        val age = 15
    ```

4.  To use a variable inside a print statement surround it with _`{}`_
    ```kotlin
       println("Age of a Surya is ${age}")
    ```
5.  Use a `repeat()` function to repeat an instruction for 'n' number of times. This is one of a kind of **loops**

    ```kotlin
        printSigns(){
            //prints + sign for 50 times
            repeat(50){
                print("+")
            }
        }
    ```

    - To create a **Nested loop** use _`repeat()` inside a `repeat()`_
      ```kotlin
      //print the layers of the cake age times
      fun printCakeBottom(age: Int, layers: Int) {
         repeat(layers) {
            repeat(age + 2) {
             print("@")
            }
            println()
         }
      }
      ```
