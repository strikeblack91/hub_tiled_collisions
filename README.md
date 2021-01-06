# Tiled

Tiled is a 2D map level editor which can create 2D map for RPG, platformers and others games.\
Tiled is highly flexible. It can be used to create maps of any size, with no restrictions on the number of layers or assets that can be used.\
It can also generate files with different informations about the created map.\

## What is the goal of this Workshop ?

We are going to use Tiled, to generate create a 2D map with collisions in C, that you could use for your Epitech games.

## What are you going to learn ?

You are going to learn:

- How to use Tiled
- How to generate and use JSON files
- Python, by creating a simple script, which will parse a JSON file

# Create a 2D map

## Step. 1 - Download

[Here](https://snapcraft.io/tiled)

## Step. 2 - Create your first Tileset

Before creating a map, we need to create Tiles !\
Tiles are the "composants" that we are going use to create a map, so let's create a new one !\
\
Create a new Tileset by clicking on "**New Tileset**".\
\
Fill the informations needed.\
There is already assets on the repository (16x16.)

## Step. 3 - Create your first (beautiful) map

Now that you have your Tileset, you can create your first map.\
\
Create a new Map by clicking on "**New Map**".\
\
Fill the informations needed.\
\
100 * 100 is big (Map size)... 

## Step. 4 - Be an artist

Now that you have your Tileset, you can create your first map.\
You should have 2 layers:
- Collision
- Background

## Step. 5 PNG and JSON

You almost finished the first part of this Workshop !\
Now, export your project as PNG and JSON.\
\
Export your Map as PNG by clicking on "**File**", "**Export as image**", select PNG and export (pay attention about the different options selected).
\
Export your Map as JSON by cliking on "**File**", "**Export as ...**", select JSON (.json) and export.
\
Good job guys ! We have everything we need to start our Python script !

# Generate collision for a C project

## JSON file ?

We generated a JSON file with Tiled of our Map, which contain severals information. We will use these informations to create an array of collisions in C !\
\
Take a look on the JSON file, how it's organised ...\
\
Then let's use Python, which is a very easy programming language, to create the C array !.

## Step. 1 - Open a file

Create your Python script, then open your JSON file.\
\
[Here a full tutoriel to open files with Python](https://en.lmgtfy.com/?q=open%20file%20python)

## Step. 2 - Parameters ?

You could customize your script a bit, by giving the name of the file as argument in the command line.\
\
```import sys```

## Step. 3 - Load JSON

Now that you have your file loaded, load the JSON content from it (1 line of code).\
\
```import json```

## Step. 4 - Get informations from JSON

Now that you have the JSON content loaded, we can get informations from it.\
\
Loop on the layers until the "**Collision**" layer, then save theses 3 informations:
- height
- widht
- data
\
What is data ? Print it, you will understand.

## Step. 5 - Create C file

Create a C file with write access (1 line of code).\

## Step. 6 - Algorithm

You have all the tools to create an algorithm, which should create a array of int, in c.\
Here an exemple of what you should/could get:
```C
const int collision[15][15] = {
	{522 ,523 ,523 ,523 ,523 ,523 ,523 ,523 ,523 ,523 ,523 ,523 ,523 ,523 ,524},
	{562 ,646 ,647 ,0 ,189 ,190 ,191 ,0 ,189 ,190 ,191 ,0 ,646 ,647 ,564},
	{562 ,686 ,687 ,0 ,229 ,230 ,231 ,0 ,229 ,230 ,231 ,0 ,686 ,687 ,564},
	{562 ,0 ,0 ,0 ,0 ,0 ,0 ,0 ,0 ,0 ,0 ,0 ,0 ,0 ,564},
	{562 ,0 ,0 ,0 ,0 ,0 ,0 ,0 ,0 ,0 ,0 ,0 ,0 ,0 ,564},
	{562 ,0 ,0 ,0 ,683 ,685 ,685 ,685 ,685 ,685 ,684 ,0 ,0 ,0 ,564},
	{562 ,0 ,0 ,0 ,721 ,563 ,0 ,563 ,0 ,563 ,725 ,0 ,0 ,0 ,564},
	{562 ,0 ,0 ,0 ,0 ,0 ,0 ,0 ,0 ,0 ,725 ,0 ,0 ,0 ,564},
	{562 ,0 ,0 ,0 ,681 ,563 ,0 ,563 ,0 ,563 ,725 ,0 ,0 ,0 ,564},
	{562 ,0 ,0 ,0 ,723 ,685 ,685 ,685 ,685 ,685 ,724 ,0 ,0 ,0 ,564},
	{562 ,0 ,0 ,0 ,0 ,0 ,0 ,0 ,0 ,0 ,0 ,0 ,0 ,0 ,564},
	{562 ,0 ,0 ,0 ,0 ,0 ,0 ,0 ,0 ,0 ,0 ,0 ,0 ,0 ,564},
	{562 ,646 ,647 ,0 ,0 ,0 ,0 ,0 ,0 ,0 ,0 ,0 ,646 ,647 ,564},
	{562 ,686 ,687 ,0 ,0 ,0 ,0 ,0 ,0 ,0 ,0 ,0 ,686 ,687 ,564},
	{602 ,603 ,603 ,603 ,603 ,603 ,603 ,603 ,603 ,603 ,603 ,603 ,603 ,603 ,604},
}
```

## Step. 7 - Can you beat me ?

[MyRPG | Epitech 2023](https://www.youtube.com/watch?v=AFMPK4B1MVs)
