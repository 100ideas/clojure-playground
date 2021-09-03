# set up
on-demand browser IDE environment guide: https://calva.io/get-started-with-clojure/
- [**START HERE**] browswer ide quick start intro --> https://gitpod.io/#https://github.com/PEZ/get-started-with-clojure
- browser ide learning clojure guide --> https://github.com/PEZ/rich4clojure
  - work thru repo full of clojure code exercises

#### linkdump
- how to set up clojure dev env for athensresearch.org code: https://handbook.athensresearch.org/community/get-involved/setup
- clojure cheatsheet - https://clojure.org/api/cheatsheet
- js -> clj translations - https://kanaka.github.io/clojurescript/web/synonym.html


# clojure from the ground up

## chapters

- ch1 intro: https://aphyr.com/posts/301-clojure-from-the-ground-up-first-principles
- ch2 types: https://aphyr.com/posts/302-clojure-from-the-ground-up-basic-types
- ch3 functions: https://aphyr.com/posts/303-clojure-from-the-ground-up-functions
- ch4 sequences: https://aphyr.com/posts/304-clojure-from-the-ground-up-sequences
- ch5 macros: https://aphyr.com/posts/305-clojure-from-the-ground-up-macros
- ch6 state (atoms): https://aphyr.com/posts/306-clojure-from-the-ground-up-state
- ch7 logistics: https://aphyr.com/posts/311-clojure-from-the-ground-up-logistics
- ch8 modeling: https://aphyr.com/posts/312-clojure-from-the-ground-up-modeling 




## notes


---

random quotes and notes expressing fundamental principles of programming languages

> To understand how type works, we’ll need several new ideas. First, we’ll expand on the notion of symbols as references to other values. Then we’ll learn about functions: Clojure’s verbs. Finally, we’ll use the Var system to explore and change the definitions of those functions

-

> A well-designed language isolates you from details you don’t need to worry about, like which logic gates or registers to use, and lets you focus on the task at hand. Good languages also need to allow escape hatches for performance or access to dangerous functionality, as we saw with Vars. 

-

> We’ve seen how let associates names with values in a particular expression, and how Vars allow for mutable bindings which apply universally. and whose definitions can change over time. We learned that Clojure verbs are functions, which express the general shape of an expression but with certain values unbound. Invoking a function binds those variables to specific values, allowing evaluation of the function to proceed.

-
 
> Functions decompose programs into simpler pieces, expressed in terms of one another. Short, meaningful names help us understand what those functions (and other values) mean.

-

> In Chapter 3, we discovered functions as a way to abstract expressions; to rephrase a particular computation with some parts missing. We used functions to transform a single value. But what if we want to apply a function to more than one value at once? What about sequences?


-

> So there’s the pieces we’d need. To glue them back together, we can use a function called cons, which says “make a list beginning with the first argument, followed by all the elements in the second argument”.

-

Chap 4

> (on map): In short, this function (`map`) expresses a sequence in which **each element is some function applied to the corresponding element in the underlying sequence**. This idea is so important that it has its own name, in mathematics, Clojure, and other languages. We call it map

-

> (on reduce): So another way to look at **reduce is like sticking a function between each pair of elements**. To see the reducing process in action, we can use reductions, which returns a sequence of all the intermediate states.

Chap 5

> ```clojure
> user=> (def x 1)
> #'user/x
> user=> x
> 1
> user=> (ignore (def x 2))
> nil
> user=> x
> 1
> ```
> def should have defined `x` to be `2` no matter what–but that never happened. At macroexpansion time, the expression `(ignore (+ 1 2))` was replaced by the expression nil, which was then evaluated to `nil`. **Where functions rewrite values, macros rewrite code.**

.

>  ss
