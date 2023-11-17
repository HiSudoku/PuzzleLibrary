# Hi Sudoku Puzzle Library

This repository contains all the Sudoku puzzles and solutions from my app [Hi Sudoku](https://hisudoku.com/).

Hi Sudoku is a free Sudoku game that offers a carefully designed puzzle library and a user-friendly experience, suitable for players of all ages.

You can download Hi Sudoku from the App Store or Google Play.


<div style="display:inline-block">
  <a href="https://apps.apple.com/app/hi-sudoku/id6450198518"><img src="res/appstore-apple.svg" alt="APP Store Button" height="70"></a>
  <a href="https://play.google.com/store/apps/details?id=com.hisudoku.classic"><img src="res/appstore-android.svg" alt="Google Play Button" height="70"></a>
</div>

## Open Source Background

As an avid Sudoku player who must play several puzzles daily to satisfy my craving, I've found that truly satisfying Sudoku games are like needles in a haystack. They often suffer from poor puzzle quality, unintuitive gameplay, or an overabundance of ads. These frustrations spurred me to **once again** develop my own Sudoku game.

After a year of dedicated effort in my spare time, I have developed this new Sudoku game, Hi Sudoku, with two main goals: a high-quality puzzle library and a comfortable user experience.

### 1. Puzzle Library

Firstly, a legitimate Sudoku puzzle must have a **unique solution**. Unfortunately, many Sudoku games nowadays don't meet this standard, leading to puzzles that may provoke the impulse to throw your phone.

Secondly, the difficulty distribution should be reasonable. The current approach of many Sudoku apps is too crude: **the fewer given numbers, the more difficult the puzzle**. This might seem logical, but it doesn't hold up. Often, it's not the start that stumps you, but the endgame when you have about 20 cells left—that's when the real challenge presents itself. If you lack advanced techniques, you'll find yourself at a dead end, forced to guess.

The principle behind Hi Sudoku's puzzle generation is simple: let the program **think like a human**. I've spent a lot of time simulating human-like solving logic and writing an algorithm that spans from simple to complex techniques, scoring puzzles based on the difficulty of the techniques required.

Hi Sudoku doesn't claim a purely handcrafted puzzle library, as manual creation is time-consuming and not necessarily the best method. Instead, I have attempted to enhance the quality of puzzles programmatically.

### 2. Gameplay

What constitutes convenient gameplay for a Sudoku app is subjective. Based on my extensive experience with numerous Sudoku games, I've optimized the operation of Hi Sudoku.

* **Highlighting**
Number highlighting is a vital feature in modern Sudoku games. The current mainstream method is to click a number on the board, highlighting all corresponding numbers and their notes. While this is already quite good, there is room for improvement. For example, if a certain number is missing from the board and you wish to highlight it, it can be challenging.
Hi Sudoku's approach allows for highlighting is by selecting the board numbers, and also by **long-pressing the number button**. You can even hold and slide on the number pad to quickly switch highlighted numbers, which is highly practical for certain solving techniques.

* **Note Mode Switching**
The conventional solution provides a toggle button to switch between entering numbers and making notes.
Hi Sudoku maintains this traditional method but also adds a new mode—**quick swipe up**. By quickly swiping up on a number button, you can temporarily switch input modes. This is especially handy in the early stages of the game, which are mainly about entering numbers, and when you occasionally need to make a note; or in the later stages, when you are mainly clearing out notes and need to confirm a number for a particular cell, a quick swipe over the corresponding number button will input it smoothly.

* **Auto Noting**
Traditional Sudoku players might view auto noting as heresy, but I believe playing Sudoku is about enjoyment, not self-torture. Hi Sudoku offers players the choice to use auto noting or not.
There are two types of auto noting: one that notes a single cell at a time and another that notes all cells at once.
For simple puzzles, noting may not be necessary. However, for tougher puzzles, auto noting can reduce the tedium of early noting, allowing you to concentrate on the fun of solving the puzzle itself.
**Tip:** There's a shortcut for auto noting—long-press the **NOTES** tool button to instantly note the selected cells.

* **Logical Hints**
This feature is a byproduct of our puzzle generation algorithm. With a set of algorithms that emulate human logic, Hi Sudoku can offer the most logical next step for the current board, along with the reasoning behind it, rather than bluntly telling you which number to place where.
**Tip:** Logical hints also have a shortcut—long-press the **MAGIC** tool button to quickly open the hint interface for a logic-based clue.

### 3. Why Open Source?

Hi Sudoku is newly born and bound to have imperfections. That's why I've decided to open source what I consider a decent puzzle library. Even if you don't fancy using Hi Sudoku, I hope you'll discover some intriguing puzzles in this library and enjoy the beauty of Sudoku.

## Puzzle Format

The puzzles are formatted in JSON, sorted into different files by difficulty. Each puzzle within the JSON files is stored as an array with two fields: `puzzle` for the original puzzle and `solution` for the answer.

Puzzles are represented as strings of 81 characters, where `.` denotes an empty cell and numbers `1 - 9` represent filled cells. The numbers are arranged by row, with the first 9 digits making up the first row, the next 9 digits the second, and so on.


## License

This puzzle library is licensed under [CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/).
