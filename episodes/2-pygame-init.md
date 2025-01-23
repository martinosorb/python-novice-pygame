---
title: "Introduction"
teaching: 10
exercises: 2
---

:::::::::::::::::::::::::::::::::::::: questions 

- 

::::::::::::::::::::::::::::::::::::::::::::::::

::::::::::::::::::::::::::::::::::::: objectives

- Python learning: how to import a library and use it.
- PyGame project: create a screen for our game.

::::::::::::::::::::::::::::::::::::::::::::::::

## Importing libraries

Good programmers write good code, but also know where they should not be writing code at all, and can reuse code instead.
One of the advantages of Python is that it has a rich community of coders that provide a wide variety of libraries for all sorts of purposes.
Because of that, when writing Python, we are mostly not starting from scratch. We can import a library instead.

In your Python file, type:

```python
import pygame
```

You'll notice that nothing seems to happen when you execute the code.
However, Python has checked that the library is installed and has imported it, meaning that its functions and variables can be accessed in subsequent code.
In other words, we can now use PyGame in our code.

We can also give libraries a nickname:

```python
import pygame as pg
```

This way, we won't need to type `pygame` in full each time we need to use one of its variables: we can write `pg` instead.

## Opening a game screen

The first that our little game requires is a screen to display the game itself.
First, we define two variables describing the desired height and width, in pixels, of our canvas.
800x600 used to be a common resolution for classic games.

```python
width = 800
height = 600
```

We then tell PyGame to initialize the screen.

```python
screen = pg.display.set_mode((width, height))
```

Notice the double parentheses. These are needed because the `set_mode` function wants a single input, which is a "tuple" of two numbers, rather than two inputs, each being a single number.
This is a rather technical distinction, which we do not need to fully understand right now.

If you execute the code as above, you might notice that a black game window opens flashes on your screen, then closes immediately.

## Our project so far

```python
import pygame as pg

width = 800
height = 600

screen = pg.display.set_mode((width, height))
```

::::::::::::::::::::::::::::::::::::::  challenge

## Exploring the Math Module

Try changing the size of the screen to make it a square.
(Then, put it back to the original size.)

:::::::::::::::  solution

## Solution

You can set, for example:

```python
width = 600
height = 600
```

:::::::::::::::::::::::::
