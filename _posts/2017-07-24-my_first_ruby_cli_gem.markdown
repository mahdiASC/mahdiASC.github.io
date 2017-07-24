---
layout: post
title:  "My First Ruby CLI Gem"
date:   2017-07-24 03:33:52 +0000
---

The following is a rundown of the process I took for creating my Ruby CLI project for the Flatiron Full Stack Web Development track.
## Brainstorming and Research
When I first read the prompt for the project, I searched for content for a simple web scrapper. I happened upon a pokemon database website and I figured I would make a simple pokedex (look up and view individual pokemon). But once I dug into the data, I found myself looking at pokemon stats and how those stats relate to the damage a pokemon does with an attack. After toying with the code, I knew I wanted to make something that users would find fun and engaging. So...I settled on remaking a pokemon battle, where the user selects their pokemon and battles a simple AI.

## Implementation
Using the Ruby gem "Nokogiri" I did a web scrape on [this pokemon site](http://pokedream.com/pokedex/pokemon?display=gen1). Using the data for each pokemon, I created a few classes:
1. PokedexPokemon : pokemon created from the raw data (no individual stats)
2. Pokedex : container for pokemon and can search through all pokedexPokemon
3. Pokemon : 'cloned' versions of a pokedexPokemon, which players can use to battle (have individual stats)

The game also required a few other classes:
1. BasePlayer : player and enemy classes derive from this base
2. Enemy : makes the enemy and controls AI functionality
3. Player : makes the player and allows player to interact with game
4. Move : each Pokemon object has a set of 4 moves (I toyed with the idea of using another web parse to create the proper moves for each pokemon, but there were too many nuances for each move with particular effects - I opted to just make simple damage-only moves for all pokemon)
5. Cli : Effectively the game object

From there, it was a matter of coding each class with its own properties and responsibilities and putting it all together in the Cli object.

One thing I struggled with was separating the CLI components (puts) away from the game logic and classes. During the course, one of the take-aways that I found helpful was the idea that although the interface between the user and your application may change (CLI, console, website, etc.) the logic behind the application remains the same.

## Fine-Tuning
Some of the bigger issues I had was understanding and implementing "best practices" for creating a Ruby Gem. The Gemfile, .gemspec, and folder organization took me by surprise near the end. 

I can absolutely appreciate abstraction, but a few of these "best practices" seemed excessive, although that's probably because the project was not done on a large scale. For example, referencing the version is typically done through a module nested within the application files, which is then referenced directly in the .gemspec file. I don't know where else this version module would be referenced, but it doesn't seem like it is anywhere else. Another confusing part was defining an empty module within the main application ruby file. It wasn't clear what the purpose of doing so was, but it was implemented on a number of projects.

Besides those few oddities, I found file organization and gem configuration to be good practice for the real thing. I'm sure I wouldn't have as much trouble if I had properly set up my files correctly from the get-go.
## Setting up the gem
The instructions for building the gem and pushing it to rubygems.org was surprisingly easy. I'll definitely try making another gem in the future! Or even revamping the pokemon game to be even more realistic.
## Final Thoughts
Coding in Ruby continues to please me. The language is very intuitive and streamlined. The fact that Ruby development is also written in Ruby is a huge plus. Besides the organization pitfalls, I felt comfortable throughout this project and found it to be good practice.
