+++
archetype = "home"
title = "Game Production"
date = 2024-09-28T15:27:29+02:00
draft = false
weight = 0
+++


## Ablauf Vorlesung
- Bauen und Debuggen der Godot Engine
- C++ Crash Course
- Struktur ausgewählter Teile einer Game Engine am Beispiel von Godot
- Seminar
  - ENTWEDER ausgewählte Themen dem Bereich Game Engine Architechture
    - Theoretisch aufarbeiten 
    - In Godot-Sourcen erklären
  - ODER ausgewählte Themen im Skripting von Game Engines
    - Theoretisch aufarbeiten
    - In Godot beispielhaft anwenden


### Ausgewählte Themen Game Engine Architecture
- Szenengraph & Traversierung
- Physik
- Animation & Animation-Blending
- Material & Shader

### Ausgewählte Themen Game-Skripting
- 3rd Person Kamera in Räumen
- NPC Pathfinding
- ...

## Resourcen

- Buch: "Game Engine Architecture" Third Edition von Jason Gregory (ISBN 9781138035454)


<!--

## Lecture Pool

- Introduction to using Godot (done in Game Production?)
- Introduction to C++
  - History of C++
  - C++ in comparison to known languages
  - Hello, World
  - Concepts
    - Header Files
      - Separating class declaration (.h) and implementation (.cpp)
    - Compiled language
    - Compiling and Linking
    - Macros
    - Pointers
    - Standard Libraries
      - Std::
      - Boost
      - Project-wise
- The DNA of an interactive application (such as a game)
  - Init Things
  - Loop forever
    - Get Input
    - Process Input to parameterize output
    - Generate output (graphics, sound, ...)
- From the scene to the graphics card.
- Understanding the Godot Initialization and Main Loop 
  - [SceneTree](https://docs.godotengine.org/en/stable/classes/class_scenetree.html#class-scenetree) is the standard [MainLoop](https://docs.godotengine.org/en/stable/classes/class_mainloop.html#class-mainloop)
  - Any MainLoop implements _initialize, _process, _physics_process and _finalize.

- Debugging into Godot
  - From WinMain to widechar_main.
  - In widechar_main: 
    - Main::Start (main/main.cpp) initializes stuff
    - os.run() runs the application main loop
  - 
   
-->

