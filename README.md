# Caarya Grand Quiz

A single-file web quiz with a live, statistics-driven analytics dashboard. Built during my software development internship at Caarya.

**[▶ Play the quiz](https://aaradhya-pathak1.github.io/caarya-grand-quiz/)**  ·  **[Read the process documentation](https://aaradhya-pathak1.github.io/caarya-grand-quiz/CaaryaPhase2.html)**

---

## What it is

A 12-question trivia quiz across three rounds that benchmarks every player against the entire pool of past participants in real time. When you finish, a terminal-style dashboard shows your global percentile, a bell curve marking where you landed, a question-by-question trail, and a score-projection matrix.

The whole application is a single self-contained HTML file. No server, no build step, no installation, you just open it.

## How it works

- **Round 1, Foundation:** five general-knowledge questions
- **Round 2, Domain Pick:** three questions from a category you choose
- **Round 3, Rapid Fire:** four questions on an eight-second timer
- **Analytics:** every attempt is written to a Firebase Realtime Database, which is read back to compute a live global percentile

## Built with

- HTML, CSS, and vanilla JavaScript (no frameworks)
- Firebase Realtime Database over the REST API
- SVG for the mathematically rendered bell curve and charts
- Web Audio API for the in-app background music

## A few engineering highlights

- **Time-adjusted percentile ranking:** score first, completion time as the tiebreaker within equal-score tiers
- **Bayesian blending:** keeps the percentile trustworthy even when only a handful of people have played, by leaning on a theoretical estimate when data is thin and trusting live data as the pool grows
- **Single-file architecture:** chosen so the project runs anywhere with zero setup; this is also why it uses the Firebase REST API rather than the SDK

## Documentation

The [process documentation](https://aaradhya-pathak1.github.io/caarya-grand-quiz/CaaryaPhase2.html) is an honest write-up of the build, focused on the bugs and decisions that taught me the most, including several that ran without any error message at all.

---

*Aaradhya Pathak · B.E. Electrical & Electronics Engineering, BITS Pilani*
