# Tasmi

**Tasmi (تسميع)** is a Quran memorization companion app, built for the [Quran Foundation Hackathon (Ramadan 2026)](https://launch.provisioncapital.com/quran-hackathon).

The name means *recitation from memory* — a student presenting what they've memorized to a teacher for review. Tasmi brings that practice into a daily companion: a structured review system that helps you build a memorization habit that lasts beyond Ramadan.

Live at [tasmi.cloud](https://tasmi.cloud).

---

## Repositories

| Repo | Description | Stack |
|------|-------------|-------|
| [`tasmi-ios`](https://github.com/tasmi/tasmi-ios) | The iOS app | Swift / SwiftUI |
| [`tasmi-auth`](https://github.com/tasmi/tasmi-auth) | OAuth2 token proxy backend | PHP 8.2 |
| [`tasmi-web`](https://github.com/tasmi/tasmi-web) | Landing page, privacy, terms | Static HTML + nginx |

---

## What it does

- **Seven-stage memorization challenges** that take a new portion from first read to long-term retention
- **Anki-style review deck** for spaced revision of previously memorized portions
- **Bookmarks, streaks, and goals** synced through Quran Foundation user APIs
- **Works across devices** — your progress follows your Quran Foundation account
- **Privacy-first** — no audio recording, no analytics tracking, no ads

---

## Tech stack

**iOS app ([`tasmi-ios`](https://github.com/tasmi/tasmi-ios))**
- Swift / SwiftUI
- [AppAuth-iOS](https://github.com/openid/AppAuth-iOS) for OAuth2 PKCE
- Keychain for token storage

**Backend ([`tasmi-auth`](https://github.com/tasmi/tasmi-auth))**
- PHP 8.2
- Stateless token proxy — no database, no user table
- Holds the Quran Foundation `client_secret` so it never ships inside the app binary

**Web ([`tasmi-web`](https://github.com/tasmi/tasmi-web))**
- Static HTML
- nginx + Let's Encrypt

---

## External APIs

- [Quran Foundation Content APIs](https://api-docs.quran.foundation) — verses, audio, tafsir, translations
- [Quran Foundation User APIs](https://api-docs.quran.foundation) — bookmarks, streaks, goals, activity
- Quran Foundation OAuth2 / OpenID Connect for authentication

---

## Built for the Quran Foundation Hackathon

Tasmi is built for the [Quran Foundation Hackathon](https://launch.provisioncapital.com/quran-hackathon), organized by Provision Launch in partnership with Quran Foundation for Ramadan 2026.

The challenge: help people maintain their connection with the Quran after Ramadan ends. Tasmi takes the traditional discipline of *tasmi'* — reciting what you've memorized to a teacher — and turns it into a daily, self-directed practice you can sustain year-round.

---

## The team

Tasmi is built by a husband-and-wife team. Issues and pull requests are welcome on individual repos. If something feels broken or missing, open an issue on the relevant repo.

## License

MIT. See `LICENSE` on each repo.
