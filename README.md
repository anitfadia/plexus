# Plexus

A playful website that helps first-year students find like-minded peers. Instead of leaving people to find their friends by chance, Plexus matches them on the interests and hobbies they actually care about, and gives them an icebreaker to start the conversation. A chatbot called **Dexter** helps with openers, club ideas and weekend plans.

**Live demo:** https://anitfadia.github.io/plexus/

## Features

- **Interest picker:** choose 3 to 8 interests from 24 options (gaming, cricket, anime, coding, music, photography and more), plus your ideal weekend vibe.
- **Match list:** the six best-matching students, ranked, each with a match percentage, the shared interests highlighted and a ready-made icebreaker.
- **Say hi:** one-click "Say hi" button on every match, with confetti.
- **Dexter, the icebreaker buddy:** a chat window that suggests openers, club ideas and weekend plans, reassures shy users and tells jokes. He uses your interests and your top match.
- **Built to feel welcoming:** bold outlines, bright colours, bouncy animations, responsive layout, keyboard-friendly, and animations switch off for people who prefer reduced motion.

## How matching works

Each student is scored against your picks:

```
shared  = interests you both picked
overlap = 2 * shared / (your picks + their interests)

score   = 35 + 14 * shared + 30 * overlap     (if you share at least one interest)
score   = 20                                  (if you share none)
score  += 6                                   (if you chose the same weekend vibe)
score   = min(score, 98)
```

The top six scores are shown, highest first. The numbers are chosen so that more shared interests clearly rank higher, while the percentage stays friendly rather than harsh.

## Run it locally

There is nothing to install. Download `index.html` and open it in a browser. The page needs an internet connection only to load the Fredoka and Nunito fonts from Google Fonts.

## Deploy on GitHub Pages

1. Put `index.html` in the root of this repo.
2. Go to **Settings, Pages**, choose **Deploy from a branch**, then `main` and `/ (root)`.
3. The site goes live at `https://<your-username>.github.io/<repo-name>/`.

## Tech

- HTML, CSS and JavaScript in a single file, with no frameworks or libraries.
- Google Fonts: Fredoka and Nunito.
- Hosted on GitHub Pages.

## Limitations

This is a front-end demo, not a finished product.

- The 12 students are **fictional**, and the page says so. Matching runs against this fixed list.
- **Dexter is scripted.** He recognises keywords such as "icebreaker", "club" and "shy", so he cannot hold a free-form conversation.
- There are no accounts, saved profiles or real messaging.

## Roadmap

- Sign-up and a database, so students are matched with real first-years.
- Connect Dexter to an AI service through a small backend that keeps the API key private.
- Real messaging or a way to share contact details once two people both say hi.
- Matching on more than interests, such as branch, hostel or clubs.

## Author

Built by [Anit Fadia](https://github.com/anitfadia).
matches first-year students with like-minded peers by interests and hobbies, with a chatbot called Dexter that suggests icebreakers.
