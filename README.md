# 🎮 Game Glitch Investigator: The Impossible Guesser

## 🚨 The Situation

You asked an AI to build a simple "Number Guessing Game" using Streamlit.
It wrote the code, ran away, and now the game is unplayable.

- You can't win.
- The hints lie to you.
- The secret number seems to have commitment issues.

## 🛠️ Setup

1. Install dependencies: `pip install -r requirements.txt`
2. Run the broken app: `python -m streamlit run app.py`

## 🕵️‍♂️ Your Mission

1. **Play the game.** Open the "Developer Debug Info" tab in the app to see the secret number. Try to win.
2. **Find the State Bug.** Why does the secret number change every time you click "Submit"? Ask ChatGPT: *"How do I keep a variable from resetting in Streamlit when I click a button?"*
3. **Fix the Logic.** The hints ("Higher/Lower") are wrong. Fix them.
4. **Refactor & Test.** - Move the logic into `logic_utils.py`.
   - Run `pytest` in your terminal.
   - Keep fixing until all tests pass!

## 📝 Document Your Experience

- [ ] Describe the game's purpose.
- [ ] Detail which bugs you found.
- [ ] Explain what fixes you applied.

## 📸 Demo Walkthrough

Describe your fixed game in numbered steps so a reader can follow along without watching a video:

1. **Start the game**: Select a difficulty level (Easy, Normal, or Hard) from the sidebar. The game displays the secret number range and number of attempts allowed.
2. **Enter your first guess**: Type a number in the input box and click "Submit Guess 🚀". The app shows whether your guess is correct or if it's too high or too low.
3. **Follow the hints**: The hints now correctly tell you which direction to guess: if too high, it says "Go LOWER!", if too low, it says "Go HIGHER!". Use these hints to narrow down your guess.
4. **Win the game**: Continue guessing using the hints until you find the secret number. When correct, the app shows "You won!" with balloons, displays your final score, and logs all your guesses.
5. **Start a new game**: Click "New Game 🔁" to reset the game state, generate a new secret number matching the current difficulty, and play again with a fresh attempt counter.

**Screenshot** *(optional)*: <!-- Insert a screenshot of your fixed, winning game here -->

## 🧪 Test Results

```
pytest tests/test_game_logic.py -v
============================= test session starts ==============================
tests/test_game_logic.py::test_winning_guess PASSED                      [ 33%]
tests/test_game_logic.py::test_guess_too_high PASSED                     [ 66%]
tests/test_game_logic.py::test_guess_too_low PASSED                      [100%]
============================== 3 passed in 0.01s ===============================
```

## 🚀 Stretch Features

- [ ] [If you choose to complete Challenge 4, describe the Enhanced UI changes here — a screenshot is optional]
