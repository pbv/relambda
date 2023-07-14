
# Haskelite

This project is a single-step interpreter for a small subset of the
Haskell language including integers, booleans, lists, tuples and
recursive definitions. The principal focus is on simplicity since this
is intended for teaching fundamentals of functional programming.

This project is an extended re-implementation in Elm of the [Lambda
Lessons](https://stevekrouse.com/hs.js/) by Jan Paul Posma and Steve Krouse.

The interpreter is based on *LambdaPMC* --- an abstract machine for a
pattern matching calculus (described in a paper submitted to the
PPDP'2023 conference).  If you are interested please contact me for a
draft copy.

## Language features

### Expressions

Integers, variables, arithmetic operations (`+, -, *, div, mod`),
comparisons between integers (`==`, `<=`, etc.), tuples, list enumerations
(e.g. `[1..10]`) and lambda-expressions.

### Function definitions

Pattern matching over integers, lists and tuples; boolean guards; recursive
definitions are allowed.

## Standard Prelude

Definitions for the following functions from the Standard Prelude are provided.

~~~haskell
even, odd :: Int -> Bool
max, min :: Int -> Int -> Int
fst :: (a,b) -> a
snd :: (a,b) -> b
(&&), (||) :: Bool -> Bool
head :: [a] -> a
tail :: [a] -> [a]
(++) :: [a] -> [a] -> [a]
length :: [a] -> Int
reverse :: [a] -> [a]
sum, product :: [Int] -> Int
take, drop :: Int -> [a] -> [a]
concat :: [[a]] -> [a]
repeat :: a -> [a]
cycle :: [a] -> [a]
iterate :: (a->a) > a -> [a]
map :: (a -> b) -> [a] -> [b]
filter :: (a -> Bool) -> [a] -> [a]
foldr :: (a -> b -> b) -> b -> [a] -> b
foldl :: (a -> b -> a) -> a -> [b] -> a
zip :: [a] -> [b] -> [(a,b)]
zipWith :: (a -> b -> c) -> [a] -> [b] -> [c]
takeWhile, dropWhile :: (a -> Bool) -> [a] -> [a]
any, all :: (a -> Bool) -> [a] -> Bool
~~~

## Not implemented

The following Haskell 98 features are *not* implemented:

* type classes 
* the numeric tower (Float, Integer, Double, etc.)
* let and case expressions
* list compreensions
* caracters and strings
* user-defined algebraic data types

----

Pedro Vasconcelos, 2023.
