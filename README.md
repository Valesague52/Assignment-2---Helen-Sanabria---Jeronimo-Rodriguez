# Assignment-2---Helen-Sanabria---Jeronimo-Rodriguez
Assignment 2 – Theory of Computation

## Students:
Helen Valentina Sanabria Guevara
Jerónimo Rodriguez Restrepo

## Versions Used
  Operating system used: Windows 11 / using WSL version 2.4 
  Compiler used: Linux Distribution - Debian 12
  Tools used: Lambda Shell Version 0.9.9.1

## Description
This assignment demonstrates the use of λ-calculus to represent and manipulate natural numbers using Barendregt numerals. We implemented and tested the combinators "succ", "pred", and "iszero" and verified their correctness through various evaluations using Lambda Shell.

## Overview
This assignment uses λ-calculus to work with Barendregt numerals. We implemented and tested:
  succ: returns the successor of a number.
  pred: returns the predecessor of a number.
  iszero: returns true if the number is zero, false otherwise.

## Instructions to Run the Solution
1. Open Lambda Shell from your terminal.
2. Load the required definitions using the following command:
   :load prelude.lam
3.You can now evaluate the following expressions:

> succ
\n f x. f (n f x)

> succ four
\f x. f (f (f (f (f x))))

> let t = plus two three
> t
\f x. f (f (f (f (f x))))

> succ t
\f x. f (f (f (f (f (f x)))))

> pred
\n f x. n (\g h. h (g f)) (\u. x) (\u. u)

> pred seven
\f x. f (f (f (f (f (f x)))))

> pred t
\f x. f (f (f (f x)))

> iszero
\m. m (\x t_0 f. f) true

> iszero t
false

> iszero zero
true


These expressions test the implementation of:
-Successor function (succ)
-Predecessor function (pred)
-Zero-check function (iszero)
-Addition (plus) as defined in the prelude.lam file.   

 ## Repository Contents
This repository contains only the essential files for this assignment:
  README.md – This documentation file
  prelude.lam – Lambda calculus definitions used for evaluation

## References
Official Lambda Shell Index & Documentation:
  https://github.com/asr/lambda-shell/blob/main/home/index.html
No other sources, AIs, articles, or repositories were consulted. All definitions and tests are based on the official materials provided for Lambda Shell.
