# In Between The Lines

> Mobile puzzle game made in Unity for the *Mobile Games* course · Game Design & Development, URJC · 2025/26

![Unity](https://img.shields.io/badge/Unity-6-black?logo=unity) ![C#](https://img.shields.io/badge/C%23-purple?logo=csharp) ![Android](https://img.shields.io/badge/Platform-Android-green?logo=android)

<!-- TODO Iván: add a GIF recorded on the phone, e.g. ![Gameplay](docs/gameplay.gif) -->

## About

A collection of short puzzles you solve **with the phone itself**: tilt it, shake it, turn it, blow into the microphone or hold your fingers on the screen. Each level mixes puzzles in different variations, and your best scores go to a local ranking.

## Puzzles

| Puzzle | How you play it |
|---|---|
| Balloon | Blow into the **microphone** to inflate it to the target size |
| Compass | Turn the phone until the dial points the right way (**gyroscope**) |
| Signal | Rotate the phone to find the signal (**gyroscope**) |
| Bottle | **Tilt** the phone to control the liquid (**accelerometer**) |
| Fishing, Darkness, Ice | **Shake** the phone (accelerometer peaks, not static tilt) |
| Elastic | Press, hold and stretch on the **touch screen** |
| Water leak | Cover the leaks by **holding fingers** on them (multi-touch) |
| Overload | **Tap** fast to keep the needle in range |

## Technical highlights

- **Unified input layer** (`InputManager`): gyroscope/attitude, accelerometer, microphone and touch, with keyboard/mouse fallbacks so every puzzle can be tested in the editor
- **Extensible puzzles**: every puzzle inherits from `PuzzleBase`; levels are configured with `LevelConfig` data
- **Menu state machine** (State pattern): `IMenuState` with Main, Mode select, Ranking, Settings and Credits states
- **Local ranking** saved as JSON (`ScoreManager`, `PlayerPrefs`)
- Sound library + `AudioManager`, scene transitions, tutorial, particles and UI animations (DOTween)

## My role

Programmer. <!-- TODO Iván: detalla qué parte hiciste tú y qué hicieron tus compañeros (el proyecto es del "Grupo1"). -->

## Tech

Unity 6 (6000.2) · C# · Android · DOTween · JsonUtility

## Running it

1. Open `Moviles3_InBetweenTheLines` with **Unity 6000.2.x**.
2. Open `Assets/_Game/Scenes/SplashScene.unity` (or `MainMenu.unity`) and press Play (keyboard/mouse fallbacks work in the editor), or build for Android to use the real sensors.
