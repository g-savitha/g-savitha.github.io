---
title: "Bit Tricks"
date: 2021-02-25T15:58:11+05:30
draft: true
tags: ["ds-algo", "programming", "competitive-programming"]
categories: [dsa, bit-magic]
sources: []
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

## Bitwise Operators Basics

Bitwise operators work on binary representation of numbers. They mainly work on individual bits of a number that is passed to these operators.

> Note: Java represents bits in 32-bit integer format

- **AND (&)** : returns 1 if both the bits are 1
- **OR (|)** : returns 1 if either of the bits is 1
- **XOR (^)** : returns 1 when both of the bits are different. (1 ^ 0 = 1)
- **NOT (~)** : inverts the bit

  ```java
  int x = 1;
  System.out.println(~x); // output: -2

  ```

  - ```
    x : 0000....1
    ~x : 1111....0 (31 1s and one 0)
    ```

  - To guess the output we must know how signed numbers are stored in java
  - In java _negative numbers_ are stored in _2's complement representation_.
  - Range of int : `-2^31 to 2^31-1 or -2,147,483,648 to 2,147,483,647`
    - Representation of `~x = 2^32 - x`
  - Positive numbers are simply stored by doing _Decimal to binary conversion_
  - > Tip: If left most bit is "0" then its a _positive number_, if its "1" then its a _negative number_

  - So from the above program ~1 is represented as
    - (2^32 - 1) -1[(2^32 -1) is thirty one 1s in ~1] => 2^32 -1 - 1 => `2^32 - 2`. So our output from the above equation would be -2.
  - One more example: 2^3 -1 = 7 (has 3 1s)

  - ```java
    int x = 5;
    System.out.println(~x); // output: -6 => (2^32 -1) -5 => 2^32 - 6
    ```

- **Left Shift (<<)** : Takes a number whose binary bits to be shifted by particular number of times.

  - `x<<1` => shift bits of number x by 1 position towards left
  - `x<<3` => shift bits of number x by 3 positions towards left
  - ```
    x    : 00000...01
    x<<1 : 00000..010
    ```
  - ```java
    int x = 3;
    x << 1; //6
    x <<2; //12
    int y = 4;
    int z = x << y //48
    ```
  - What happem=ns when you shift number 3 by 30 ?
    - `3 << 30` => 110000...0 (30 0s are added at the end moving 1s to the beginning)
    - May get a negative number. If leading bits are 1.
  - **Left shift of `x << n = x * 2^n`** for smaller numbers. For larger numbers leading bits will be 1 , which might be considered as negative numbers (in such cases we dont get exact multiples of 2).

- **Right Shift(>>)** : This is opposite of left shift. Shifts all the bits to right by the given position.
  - ```
    x    : 00...10001
    x>>1 : 000..10000
    ```
  - ```java
    x = 33;
    x >> 2; //8
    ```
  - An interesting thing happens when it comes to negative numbers. We have another operator called _unsigned right shift_ for _negative numbers_.
  - This particular right shift (`>>`) is also called _signed right shift_ (because it treats negatives and positives differently.)
    - In case of _positives_ : It fills leading bits with `0`
    - In case of _negatives_ : It fills trailing bits with `1` to keep the sign.
    - ```
      x = -2;
      x >> 1; // -1
      ```
    - ```
      x = -2: represented as 2^32 - 2 in 2's compliment form
       x      : 11111....10 => 31 1s and 1 0
       x >> 1 : 11111....11 (fills the leading bit with 1 since the number is -ve) => 32 1s
      ```
  - **Unsigned right shift operator** `>>>` : Shifts bits to the right based on given positions
    - Difference between previous one and this one is, this _fills leading bits with 0_.
    - ```
      x = -2;
      x>>>1; // 2147483647
      ```
    - ```
       x = -2: represented as 2^32 - 2 in 2's compliment form
       x       : 11111....10 => 31 1s and 1 0
       x >>> 1 : 01111....11 (fills the leading bit with 0 since the number is +ve) => 31 1s (2^32 - 1) and leadin 0
      ```
    - **Right shift of `x >> n = x /2^n`**

---

## Worth checking out

[Hackerearth tutorial on bit manipulation](https://www.hackerearth.com/practice/basic-programming/bit-manipulation/basics-of-bit-manipulation/tutorial/)
[Bitwise algorthms](https://www.geeksforgeeks.org/bitwise-algorithms/)
