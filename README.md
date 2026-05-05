# IT3040 – ITPM Assignment 1
## Singlish to Sinhala Transliteration Accuracy Testing

**Student:** Kavindu Chamuditha  
**Registration Number:** IT23315150  
**Degree:** BSc (Hons) in Information Technology – Year 3  
**Module:** IT3040 – IT Project Management 

---

## 📌 Assignment Overview

This assignment evaluates the accuracy of the **Chat Sinhala transliteration** function of the live web application available at:

🔗 [https://www.pixelssuite.com/chat-translator](https://www.pixelssuite.com/chat-translator)

The objective is to identify **50 negative test cases** where the system fails to correctly convert chat-style **Singlish** (romanized Sinhala) input into proper **Sinhala** output. All 24 Singlish input types specified in the assignment guidelines are covered, with a minimum of 2 test cases per type.

---

## 📁 Repository Structure

```
Playwright-Testing-Assignment/
│
├── test_automation.py          # Main Playwright automation script
├── IT23315150.xlsx             # Completed test cases Excel file (50 negative test cases)
└── README.md                   # This file
```

---

## ✅ Prerequisites

Before running the tests, make sure you have the following installed:

- **Python 3.11 or 3.12** – [Download here](https://www.python.org/downloads/)
- **Google Chrome** (recommended) or Chromium
- **Anaconda** (optional but recommended for environment management)

---

## ⚙️ Installation

Open **Command Prompt** and run the following commands one by one:

### Step 1 – Upgrade pip
```bash
"C:\Users\<YourUsername>\anaconda3\python.exe" -m pip install -U pip
```

### Step 2 – Install required dependencies
```bash
"C:\Users\<YourUsername>\anaconda3\python.exe" -m pip install playwright openpyxl
```

### Step 3 – Install Playwright browsers
```bash
"C:\Users\<YourUsername>\anaconda3\python.exe" -m playwright install
```

> **Note:** Replace `<YourUsername>` with your actual Windows username. If you are not using Anaconda, simply use `python` instead of the full path.

---

## ▶️ How to Run the Tests

### Step 1 – Navigate to the project folder
```bash
cd "path\to\Playwright-Testing-Assignment"
```

### Step 2 – Run the automation script
```bash
"C:\Users\<YourUsername>\anaconda3\python.exe" test_automation.py --excel "IT23315150.xlsx" --url "https://www.pixelssuite.com/chat-translator" --wait-ms 5000 --type-delay-ms 80 --slow-mo-ms 200 --save-every 1 --keep-open
```

### What happens when you run it:
1. A **Chromium browser** opens automatically
2. The script navigates to the chat translator website
3. Each of the 50 Singlish inputs is typed one by one
4. The actual Sinhala output is captured from the website
5. The output is compared with the expected Sinhala translation
6. **PASS** or **FAIL** status is written into the Excel file automatically
7. Press `CTRL+C` to stop once all 50 rows are completed

---

## 📊 Test Cases Overview

The Excel file `IT23315150.xlsx` contains **50 negative test cases** covering all 24 Singlish input types:

| # | Singlish Input Type | Count |
|---|---|---|
| 1 | Question forms | 3 |
| 2 | Command forms | 2 |
| 3 | Greetings | 2 |
| 4 | Requests | 2 |
| 5 | Responses | 2 |
| 6 | Repeated Words | 2 |
| 7 | Inputs with Punctuation Marks | 2 |
| 8 | Romanization / Spelling Variants | 2 |
| 9 | Isolated English Word Insertions in Singlish | 2 |
| 10 | Multi-Word English Phrases in Singlish | 2 |
| 11 | English Digital Terms in Singlish | 2 |
| 12 | Platform/App Names in Singlish | 2 |
| 13 | English Abbreviations/Acronyms in Singlish | 2 |
| 14 | English Clipped Forms in Singlish | 2 |
| 15 | Place Names Embedded in Singlish | 2 |
| 16 | Person Names Embedded in Singlish | 2 |
| 17 | Inputs with Numbers and Numeric Suffixes | 2 |
| 18 | Inputs with Currency | 2 |
| 19 | Inputs with Time Formats | 2 |
| 20 | Inputs with Dates | 2 |
| 21 | Inputs with Unit of Measurements | 2 |
| 22 | Inputs with Slang and Casual Phrasing | 2 |
| 23 | Online Identifiers in Singlish | 2 |
| 24 | Inputs Containing Emojis | 3 |
| | **Total** | **50** |

### Excel Column Structure

| Column | Description |
|---|---|
| A | TC ID (e.g., Neg_0001) |
| B | Input length type (S / M / L) |
| C | Input (Singlish text) |
| D | Expected output (correct Sinhala) |
| E | Actual output (filled by Playwright) |
| F | Status (PASS / FAIL – filled by Playwright) |
| G | Singlish input types covered |
| H | Evidence or rationale for the input type covered |

---

## 🔧 Command Line Arguments

| Argument | Description | Default |
|---|---|---|
| `--excel` | Path to the Excel test cases file | `Assignment 1 - Test cases.xlsx` |
| `--url` | URL of the application to test | PixelsSuite chat-translator |
| `--wait-ms` | Wait time (ms) after each transliteration | `5000` |
| `--type-delay-ms` | Delay (ms) between each keystroke | `80` |
| `--slow-mo-ms` | Slow motion delay (ms) for browser actions | `200` |
| `--save-every` | Save Excel after every N rows | `1` |
| `--keep-open` | Keep browser open after test completion | `false` |
| `--headless` | Run browser in headless mode (no UI) | `false` |

---

## 📝 Notes

- All 50 test cases are **negative test cases** — the translator is expected to **FAIL** on all of them
- Input length categories: **S** (≤ 30 characters), **M** (31–299 characters), **L** (300–450 characters)
- TC IDs for negative test cases begin with `Neg_`
- None of the test inputs are taken from the examples provided in the assignment Appendix 1 or Appendix 2
- The test cases cover real-life Sri Lankan daily chat scenarios including tech issues, study life, travel, food, sports, and social interactions

---

## 👤 Author

**Kavindu Chamuditha**  
IT23315150  
BSc (Hons) in Information Technology  
Sri Lanka Institute of Information Technology (SLIIT)