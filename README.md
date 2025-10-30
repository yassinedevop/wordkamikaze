
# WordKamikaze (Word Autocomplete Assistant)


## Overview

`WordKamikaze` is a Python script that provides smart **word suggestions** and simulates human-like typing based on a user’s input prefix.
It features:

* Dictionary-based prefix matching
* Humanized typing delay (with micro-pauses and variable speed)
* Toggleable autocompletion
* Transparent GUI displaying the current input and suggestion
* Hotkey control to enable/disable the tool dynamically

---
## Demo

<video src="https://vimeo.com/1132233055?share=copy&fl=sv&fe=ci" width="320" height="240" controls></video>

## ⚙️ Installation

1. **Clone the repository:**

   ```bash
   git clone https://github.com/yassinedevop/wordkamikaze.git
   cd wordkamikaze
   ```

2. **Install dependencies:**

   ```bash
   pip install pynput
   ```

   `tkinter` is included with most Python installations.
   If not, install it according to your OS (e.g., `sudo apt install python3-tk` on Ubuntu).

3. **Prepare your dictionary:**
   Create a text file named `dict.txt` in the same folder.
   Each line should contain a valid English word:

   ```
   apple
   banana
   carrot
   ...
   ```

---

## 🚀 Usage

1. Run the script:

   ```bash
   python wordkamikaze.py
   ```

2. A small transparent window will appear at the top center of your screen showing:

   * The current input prefix
   * The best matching suggestion
   * The activation status `[Active]/[Inactive]`

3. Type in any application.
   When you type something like `3par`, the script will:

   * Parse it as: “use the first 3 letters of ‘par’ as prefix”
   * Search for matching words in `dict.txt`
   * Autocomplete the best match naturally (letter by letter)

4. **Toggle On/Off:**
   Click the `[Active]` label or press **Ctrl + Alt + T** to toggle autocompletion.

5. **Exit:**
   Press **Esc** to close the program.

---

## 🧩 How It Works

* Uses **pynput** to listen for keyboard input and simulate keystrokes.
* Matches prefixes using a simple parsing rule (e.g., `2bl` → prefix `"bl"` of length 2).
* Filters out previously used words to avoid repetition.
* Simulates natural typing speed with configurable randomness to mimic human typing rhythm.



## 🧰 Configuration

You can tweak typing realism in the class `WordAutocomplete`:

```python
BASE_CHAR_DELAY = 0.03       # Base delay between characters
CHAR_DELAY_VARIANCE = 0.03   # Random variation
WORD_DELAY = 0.15            # Pause after a word
PAUSE_PROBABILITY = 0.2      # Chance for micro-pauses
MICRO_PAUSE = 0.08           # Duration of micro-pause
```


---

## ⚖️ Ethical Disclaimer

> This project was created for **educational and research purposes only**.
> It should **not** be used to gain unfair advantage in any online competitive environment or to violate the Terms of Service of any platform.
> The author is **not responsible** for any misuse of this tool.

If you wish to explore automation safely, try integrating this script into **local games or typing experiments** instead.

---
