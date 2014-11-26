---
layout: page
title: Scrabble
---

## Expectations

* Work on the exercise defined below for 30 minutes with your facilitator
* The facilitator may change the spec or ask additional questions to assess your understandings/skills
* As you work, you may:
  * Ask questions of your facilitator
  * Reference external public resources (ie: Google, Ruby API, etc)
  * Use the tooling most comfortable to you (Editor/IDE, testing framework, support tools like Guard, etc)
* As you work, you should not:
  * Copy code snippets other than those present in this description
  * Seek live support from individuals other than your facilitator

## Getting Started

Because of the compressed timeline, we've created a starter repo with some of the grunt work taken care of. Begin by cloning the repo from GitHub and running `bundle` to install dependencies:

{% terminal %}
$ git clone https://github.com/turingschool/scrabble
$ cd scrabble
$ bundle
{% endterminal %}

## Sample Exercise

During the assessment, complete an exercise similar to the one below.

### Word Scoring

Let's use test-driven development to build pieces of a Scrabble-like game.

Create functionality to score words based on the following letter values:

```plain
Letter                           Value
A, E, I, O, U, L, N, R, S, T       1
D, G                               2
B, C, M, P                         3
F, H, V, W, Y                      4
K                                  5
J, X                               8
Q, Z                               10
```

Or, represented by a Ruby hash:

```ruby
{
  "A"=>1, "B"=>3, "C"=>3, "D"=>2,
  "E"=>1, "F"=>4, "G"=>2, "H"=>4,
  "I"=>1, "J"=>8, "K"=>5, "L"=>1,
  "M"=>3, "N"=>1, "O"=>1, "P"=>3,
  "Q"=>10, "R"=>1, "S"=>1, "T"=>1,
  "U"=>1, "V"=>4, "W"=>4, "X"=>8,
  "Y"=>4, "Z"=>10
}
```

Create your solution:

* using Test-Driven Development with MiniTest or RSpec
* insensitive to case
* such that an empty word or `nil` scores `0`
* using this interaction model:

{% irb %}
> game = Scrabble.new
=> ...
> game.score("hello")
=> 8
> game.score("")
=> 0
> game.score(nil)
=> 0
{% endirb %}

## Evaluation

Subjective evaluation will be made on your work/process according to the following criteria:

### 1. Ruby Syntax & API

* 4: Developer is able to comfortably implement solutions using the best-choice tools Ruby has to offer
* 3: Developer is able to comfortably implement solutions in Ruby
* 2: Developer is generally able to write Ruby, but gets stuck on or needs help with fundamental concepts
* 1: Developer spends significant time debugging elementary syntax or concepts

### 2. Ruby Style

* 4: Developer solves problems with a balance between conciseness and clarity
* 3: Developer writes code that is easy to follow
* 2: Developer writes code that has unnecessary variables, operations, or steps which do not increase clarity
* 1: Developer writes code that is difficult to understand

### 3. Blocks & Enumerations

* 4: Developer is able to consistently select and implement the best-choice enumerator methods with blocks
* 3: Developer demonstrates understanding of blocks and can effectively use enumerable methods
* 2: Developer can use enumerator methods, but struggles to choose the right one for the job or demonstrates weak understanding of blocks
* 1: Developer is not able to use enumerator methods or blocks to solve the problem at hand

### 4. Testing

* 4: Developer consistently takes small steps, using the tests for *both* design and verification
* 3: Developer uses tests to guide development in small chunks
* 2: Developer uses tests to guide development, but does not break features down into small problems
* 1: Developer does not integrate testing throughout their development process

### 5. Workflow

* 4: Developer is a master of their tools, efficiently moving between phases of development
* 3: Developer demonstrates comfort with their tools and makes some use of keyboard shortcuts
* 2: Developer smoothly moves between tools, but is dependent entirely on mouse-driven interaction
* 1: Developer gets work done, but wastes significant time or screen real estate

### 6. Collaboration

* 4: Developer *actively seeks* collaboration both before implementing, while in motion, and when stuck
* 3: Developer lays out their thinking *before* attacking a problem and integrates feedback through the process
* 2: Developer asks detailed questions when progress slows or stops
* 1: Developer is able to integrate unsolicited feedback but does not really collaborate
