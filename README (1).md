# IELTS Word Master 📚

A mobile-first flashcard app for mastering **Academic Word List (AWL)** vocabulary — built with vanilla HTML, CSS, and JavaScript. No frameworks, no build tools, no dependencies.

🔗 **Live demo:** [yers1.github.io/ielts-word-master](https://yers1.github.io/ielts-word-master)

## ✨ Features

- **50 AWL words** from Sublists 1–3, each with definitions, example sentences, synonyms, and collocations
- **Two study modes** — Flashcard (flip) and Quiz (multiple choice)
- **SM-2 Spaced Repetition** — the same algorithm used by Anki, so you review words at the optimal time
- **🔊 Pronunciation** — uses the browser's built-in Speech Synthesis API (British English)
- **⭐ Saved Words** — bookmark words to review later
- **🔥 Streak tracking** — daily study streak counter
- **Progress bars** — track how many words you've seen per sublist
- **Persistent state** — progress is saved in `localStorage`

## 🚀 Getting Started

No installation needed. Just open `index.html` in your browser:

```bash
# Clone the repo
git clone https://github.com/Yers1/ielts-word-master.git

# Open in browser
open index.html
# or just double-click index.html in your file explorer
```

## 🌐 Deploy to GitHub Pages

1. Push to GitHub
2. Go to **Settings → Pages**
3. Set source to `main` branch, root folder
4. Your app will be live at `https://yers1.github.io/ielts-word-master`

## 📁 File Structure

```
ielts-word-master/
├── index.html   # Everything in one file — HTML, CSS, and JS
└── README.md
```

## 🧠 How SM-2 Works

After revealing a flashcard, rate your recall:

| Button | Quality | Next review |
|--------|---------|-------------|
| Again  | 1       | Tomorrow    |
| Hard   | 2       | Tomorrow    |
| Good   | 4       | Days later (grows each time) |
| Easy   | 5       | Even longer interval |

Words you struggle with come back sooner. Words you know well are spaced further apart.

## 📖 Word Coverage

| Sublist | Words | Topics |
|---------|-------|--------|
| AWL 1   | 30    | Most frequent academic words |
| AWL 2   | 10    | Common academic vocabulary   |
| AWL 3   | 10    | Extended academic vocabulary |

## 🛠️ Extending the App

To add more words, find the `WORDS` array in `index.html` and add objects following this structure:

```js
{
  id: 51,
  word: "theory",
  type: "noun",
  sub: 1,
  def: "A system of ideas intended to explain something",
  ex: "Darwin's theory of evolution changed how we understand life on Earth.",
  syn: ["hypothesis", "idea", "framework"],
  col: "in theory · theoretical framework · develop a theory"
}
```

## 📄 License

MIT — free to use, modify, and share.
