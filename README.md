# wordle solver

a fast, intelligent wordle solver built with tauri. helps you find the best word suggestions based on your guesses and feedback.

## what it does

this app analyzes your wordle guesses and provides optimal word suggestions to help you solve the puzzle. it uses letter frequency analysis and smart filtering to narrow down possibilities with each guess.

## features

- real-time word suggestions based on your guesses
- intelligent scoring system using letter frequency
- tracks possible remaining words
- clean, modern ui with dark mode
- built with tauri for native performance
- works offline once installed

## how to use

1. enter your guess letters (5 letters)
2. mark each letter with its status:
   - ● correct (green) - right letter, right position
   - ◐ present (yellow) - right letter, wrong position  
   - ○ absent (gray) - letter not in word
   - ? unknown - not sure yet
3. click "add" to submit your guess
4. click "get suggestions" to see optimal next words
5. repeat until you solve it

## installation

```bash
npm install
npm run dev
```

for production build:

```bash
npm run tauri build
```

## tech stack

- tauri for desktop app framework
- vanilla javascript for logic
- html/css for ui
- rust backend
- custom wordle solving algorithm

## how the solver works

the solver uses a multi-step approach:

1. starts with a database of valid wordle words
2. filters possible answers based on your feedback
3. calculates letter frequency across remaining words
4. scores potential guesses by how much information they provide
5. suggests words that maximize information gain

the algorithm considers position-specific letter matching, handles duplicate letters correctly, and prioritizes words with common starting letters.

## performance

should be very fast. filtering and suggestions happen instantly even with thousands of possible words.
