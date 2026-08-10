# German Trainer

A desktop multiple-choice practice app for learning German, covering levels **A1 → C1** across translation and grammar questions.

![Python](https://img.shields.io/badge/python-3.x-blue)
![Platform](https://img.shields.io/badge/platform-cross--platform-lightgrey)
![License](https://img.shields.io/badge/license-MIT-green)

## Features

- **Multiple-choice quiz format** — four options per question, instant feedback with the correct answer highlighted
- **Two question modes** — Translation and Grammar (or Mixed, to draw from both)
- **Skill filtering** — narrow grammar questions down to a specific skill (e.g. cases, verb conjugation, word order)
- **Level filtering** — enable any combination of A1, A2, B1, B2, and C1 to control question difficulty
- **Explanations** — every question includes a short explanation shown after you answer
- **Score tracking** — running score and percentage, with a one-click reset
- **Question history** — step back through previous questions with "Previous," including your past answers
- **Skip / Next controls** — move on from a question at any time

## Getting Started

### Requirements

- Python 3.x
- `tkinter` (included with most Python installations)

### Running

```bash
python german_trainer.py
```

## Question Bank

Questions are loaded from `german_trainer_question_bank.json`, which must be placed in the same folder as the script. The trainer expects a JSON object with a `questions` array, where each question looks like:

```json
{
  "id": 1,
  "level": "A2",
  "mode": "grammar",
  "skill": "verb_conjugation",
  "question": "Ich ___ jeden Tag Kaffee.",
  "options": ["trinke", "trinkst", "trinkt", "trinken"],
  "answer": "trinke",
  "explanation": "First-person singular (ich) takes the -e ending: ich trinke."
}
```

| Field | Description |
|---|---|
| `id` | Unique question identifier |
| `level` | CEFR level (`A1`–`C1`) |
| `mode` | `"translation"` or `"grammar"` |
| `skill` | Grammar topic (used for skill filtering; any value for translation questions) |
| `question` | The prompt text shown to the user |
| `options` | Array of exactly 4 answer choices |
| `answer` | The correct option (must exactly match one entry in `options`) |
| `explanation` | Shown after answering, regardless of correctness |

## Usage

1. Choose a **Mode** (Mixed, Translation, or Grammar) from the top toolbar
2. If you're in Grammar or Mixed mode, optionally narrow by **Skill**
3. Check/uncheck **Levels** to control which CEFR levels appear
4. Click an answer to see instant feedback and an explanation
5. Use **Next question**, **Skip**, or **Previous** to navigate
6. Track your progress with the score counter in the top-right, or click **Reset score** to start over

## License

MIT — see [LICENSE](LICENSE) for details.
