# 🎮 Varthix Tic-Tac-Toe AI

**Unbeatable Tic-Tac-Toe AI** — built for the SAM AI Technologies Internship (Task 4, extended).

A from-scratch minimax engine with alpha-beta pruning, wrapped in a branded, animated single-page interface — with a live readout into how the AI is actually thinking each turn.

🔗 **Live Demo:** [thodetivarshith.github.io/SAM-AI-TicTacToe-AI](https://thodetivarshith.github.io/SAM-AI-TicTacToe-AI/)
👤 **Author:** [Varshith](https://github.com/thodetivarshith)

---

## ✨ Features

| Category | What it does |
|---|---|
| 🧠 **Minimax + Alpha-Beta Pruning** | Full game-tree search — the AI simulates every possible line of play and picks the move that guarantees its best outcome |
| 🎯 **3 Difficulty Levels** | Easy (mostly random), Medium (weakened search, genuinely beatable), Unbeatable (never loses) |
| 📊 **Live Engine Readout** | Nodes evaluated, search depth, positions pruned, evaluation score, think time — for every AI move, in real time |
| 📈 **Evaluation Bar** | Visualizes who the current position favors |
| 🔥 **Move Heatmap** | Optional overlay showing how the AI scored every candidate move |
| 🕘 **Move History** | Every move logged with player and cell |
| ↩️ **Undo** | Roll back the last round (your move + AI's reply) |
| 🏆 **Score Tracking** | Wins / draws / losses tracked across the session |
| 🔊 **Synthesized Sound** | Web Audio–generated sound effects — no external audio files |
| 🎉 **Win Celebration** | Canvas-based confetti burst and glowing win-line animation |
| 🎨 **Branded Animated UI** | Ambient canvas background, glassmorphic panels, flowing gradient accents |

---

## 🖥️ Tech Stack

**HTML, CSS, and vanilla JavaScript** — a single self-contained file, no build step, no dependencies, no external libraries. Fonts load from Google Fonts; everything else (animation, audio, game logic) is native browser APIs (Canvas, Web Audio).

---

## 🚀 Run Locally

No installation needed — it's one static file.

```bash
git clone https://github.com/thodetivarshith/SAM-AI-TicTacToe-AI.git
cd SAM-AI-TicTacToe-AI
```

Then either:
- Double-click `index.html` to open it directly in your browser, or
- Use VS Code's "Live Server" extension for auto-reload while editing

---

## ☁️ Deployment

Deployed on **GitHub Pages** directly from the `main` branch (`/root`) — no build pipeline required since it's plain HTML/CSS/JS.

To redeploy after changes: push to `main`, and GitHub Pages rebuilds automatically within a minute or two.

---

## 🧠 How the AI Works

- **Minimax:** the AI recursively simulates every possible sequence of moves through to the end of the game, assuming both players play optimally, and picks the move that guarantees its best possible outcome.
- **Alpha-beta pruning:** once the search finds a branch that can't possibly beat a move it's already found, it stops exploring that branch. This doesn't change the result — it just makes the search dramatically faster. The "Positions pruned" stat in the live readout shows this happening in real time.
- **Scoring:** a finished game scores `+10 - depth` for an AI win, `depth - 10` for a human win, and `0` for a draw. Subtracting depth biases the AI toward winning quickly and losing slowly (if a loss is forced).
- **Correctness:** stress-tested by simulating 300 games of random-play human vs. Unbeatable difficulty — zero losses, consistent with a correct minimax implementation on a fully-solved game like Tic-Tac-Toe.

---

## 📌 About This Task

Built as part of the **SAM AI Technologies Internship** — Task 4: Tic-Tac-Toe AI.
Original brief: build a simple, unbeatable Tic-Tac-Toe AI opponent.
This build adds difficulty levels, a live search-engine readout, move history, undo, sound, and a fully animated interface.

**A note on authorship:** the core algorithm — minimax search, alpha-beta pruning, and the scoring function — reflects my own understanding of game-tree search and is something I can explain and defend in detail. The UI/animation layer (CSS effects, canvas particle system, Web Audio synthesis) was built with AI assistance, since front-end/JS isn't my primary skill set — my main focus is Python and AI/ML.

---

## 📄 License

MIT
