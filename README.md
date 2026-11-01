# Flappy Bird in C

A simple Flappy Bird clone that runs in the Windows terminal. Written in plain C with no external libraries.

---

## How to Play

| Key | Action |
|-----|--------|
| `SPACE` | Flap up |
| `Q` | Quit |

Fly through the gaps in the pipes without hitting them or the ground.

---

## Requirements

- Windows
- GCC (MinGW) or any C compiler

---

## Build & Run

```bash
gcc flappybird.c -o flappybird.exe
./flappybird.exe
```

---

## Files

| File | Description |
|------|-------------|
| `flappybird.c` | The game source code |
| `flappybirddocumentation.docx` | Line-by-line explanation of every line of code |

---

## Settings

You can change these values at the top of `flappybird.c` to adjust difficulty:

```c
#define SCREEN_WIDTH   40   // width of the game screen
#define SCREEN_HEIGHT  20   // height of the game screen
#define PIPE_GAP        6   // size of the hole in the pipe (bigger = easier)
#define PIPE_SPEED      1   // how fast the pipe moves (higher = harder)
```

---

## How It Works

The game runs a loop that repeats ~12 times per second:

1. Read keyboard input
2. Apply gravity to the bird
3. Move the pipe left
4. Check for collisions
5. Draw the frame to the terminal

The "animation" works by moving the cursor back to the top of the screen each frame and overwriting the previous frame instead of scrolling.

---

## Made for

First semester C programming course. No structs, no pointers, no external libraries — just variables, loops, functions, and if statements.
