# instructions.md

## Fenrir Arena - Online Gaming Website

**Project Owner:** Fenrir Project

**Project Type:** Online Gaming Website (Browser-based Casual Gaming Portal)

---

## 1. Project Overview

You are a web developer tasked with building **Fenrir Arena**, a browser-based gaming portal where visitors can browse a catalog of casual games, play them directly in the browser, create an account, and compete on leaderboards.

The site consists of **8 pages** and **6 playable games**, with a lightweight backend handling user accounts, score storage, and leaderboards.

**All deliverables are source code files (HTML, CSS, JavaScript, backend code) plus supporting documentation. No physical production is required.**

Your deliverables cover four categories:

- Frontend pages (8 files)

- Playable games (6 files)

- Backend service (account, score, and leaderboard endpoints)

- Documentation (README.md)

A sample Home Page layout is provided by the client as **`reference_image.png`**. Use it as a visual guide for the header, hero banner, tagline placement, and featured games section.

---

## 2. Brand Guidelines

### 2.1 Product Identity

| Field | Value |
|---|---|
| Product name | Fenrir Arena |
| Tagline | "Play. Compete. Conquer." |
| Project owner | Fenrir Project |

### 2.2 Naming Rules

- The site name **Fenrir Arena** must appear in the website header on every page

- The tagline **"Play. Compete. Conquer."** must be used verbatim on the Home Page and the About Page

- Do not rephrase or shorten the tagline

### 2.3 Colour Palette

| Use | Colour Name | Hex Code |
|---|---|---|
| Primary background | Charcoal Black | `#1A1A1F` |
| Surface / header | Wolf Gray | `#2E2E38` |
| Accent / buttons | Ember Orange | `#FF7A30` |
| Secondary accent | Frost Blue | `#4FB6E8` |
| Text | Off White | `#F5F5F7` |

### 2.4 Title Usage by Context

| Context | Title / Text |
|---|---|
| Website header (all pages) | Fenrir Arena |
| Home Page hero heading | Fenrir Arena |
| Home Page tagline text | Play. Compete. Conquer. |
| About Page tagline text | Play. Compete. Conquer. |
| Browser tab title | Fenrir Arena |

---

## 3. Page Instructions

### 3.1 Overview

- Total pages to create: **8**

- Each page must be a separate file (e.g., `index.html`, `library.html`, `login.html`, etc.)

- Every page must include the website header showing **Fenrir Arena**

- File format: **HTML + CSS + JavaScript**

### 3.2 Page Breakdown

| # | Page | File Name | Required Elements |
|---|---|---|---|
| 1 | Home Page | index.html | Hero banner, tagline, featured games section (4 games), "Browse All Games" button |
| 2 | Game Library Page | library.html | Grid of all 6 games, category filter buttons (Arcade, Puzzle, Racing), game cards with thumbnail + title + category tag |
| 3 | Individual Game Page | game.html | Embedded game canvas, game title, short description, "How to Play" section, leaderboard table (top 10) |
| 4 | Login Page | login.html | Email field, password field, Login button, link to Sign Up Page |
| 5 | Sign Up Page | signup.html | Username field, email field, password field, Create Account button, link to Login Page |
| 6 | User Profile Page | profile.html | Username display, table of personal best scores per game |
| 7 | About Page | about.html | Text section describing Fenrir Arena, tagline displayed verbatim |
| 8 | Contact Page | contact.html | Name field, email field, message field, Send Message button |

### 3.3 Per-Page Rules

**Home Page (index.html):**

- Hero banner must display the heading "Fenrir Arena"

- Hero banner must display the tagline "Play. Compete. Conquer." verbatim

- Featured games section must show exactly 4 games

- A "Browse All Games" button must link to library.html

- The layout must follow the client-provided `reference_image.png`

**Game Library Page (library.html):**

- Must display a grid containing all 6 games

- Must include category filter buttons labelled: Arcade, Puzzle, Racing

- Each game card must show: a thumbnail image, the game title, and a category tag

**Individual Game Page (game.html):**

- Must contain an HTML5 Canvas element where the game runs

- Must display the game title and a short description

- Must include a "How to Play" section with instructions

- Must include a leaderboard table showing the top 10 scores, sorted highest to lowest

**Login Page (login.html):**

- Must contain an email input field

- Must contain a password input field

- Must contain a button labelled "Login"

- Must contain a link to the Sign Up Page

**Sign Up Page (signup.html):**

- Must contain a username input field

- Must contain an email input field

- Must contain a password input field

- Must contain a button labelled "Create Account"

- Must contain a link to the Login Page

**User Profile Page (profile.html):**

- Must display the logged-in user's username

- Must display a table listing the user's best score for each game

**About Page (about.html):**

- Must contain a text section describing Fenrir Arena

- Must display the tagline "Play. Compete. Conquer." verbatim

**Contact Page (contact.html):**

- Must contain a Name input field

- Must contain an Email input field

- Must contain a Message input field

- Must contain a button labelled "Send Message"

---

## 4. Game Instructions

### 4.1 Overview

- Total games to create: **6**

- Each game must run inside an **HTML5 Canvas** element

- Each game must be controllable using **keyboard input** (arrow keys and spacebar)

- Each game must be embedded on its own Individual Game Page

### 4.2 Game Breakdown

| Game | Category | Controls |
|---|---|---|
| Brick Breaker | Arcade | Left/Right arrow keys to move paddle |
| Snake Classic | Arcade | Arrow keys to change direction |
| Memory Match | Puzzle | Mouse click to flip cards |
| 2048 Tile Merge | Puzzle | Arrow keys to merge tiles |
| Endless Runner | Racing | Spacebar to jump |
| Sky Dash | Racing | Arrow keys to steer, spacebar to boost |

### 4.3 Per-Game Rules

**Brick Breaker:**

- Category: Arcade

- Player controls a paddle using Left and Right arrow keys

- Game must track and display the player's current score during play

**Snake Classic:**

- Category: Arcade

- Player controls the snake's direction using arrow keys

- Game must track and display the player's current score during play

**Memory Match:**

- Category: Puzzle

- Player flips cards using mouse clicks

- Game must track and display the player's current score during play

**2048 Tile Merge:**

- Category: Puzzle

- Player merges tiles using arrow keys

- Game must track and display the player's current score during play

**Endless Runner:**

- Category: Racing

- Player jumps using the spacebar

- Game must track and display the player's current score during play

**Sky Dash:**

- Category: Racing

- Player steers using arrow keys and boosts using spacebar

- Game must track and display the player's current score during play

### 4.4 Score Submission

- When a game ends, the player's final score must be sent to the backend score endpoint

- The score must be saved only if the player is logged in

---

## 5. Backend Instructions

### 5.1 Overview

- Backend framework: **Node.js with Express**

- Database: **SQLite**

- The backend must expose endpoints for account creation, login, score saving, and leaderboard retrieval

### 5.2 Account Endpoints

- **Sign up endpoint:** accepts username, email, and password; stores the password as a hashed value

- **Login endpoint:** accepts email and password; returns a session confirming the user is logged in

- Login session must persist while the browser tab is open

### 5.3 Score Endpoints

- **Save score endpoint:** accepts username, game name, score value, and date; stores the record

- **Leaderboard endpoint:** accepts a game name; returns the top 10 scores for that game, sorted from highest to lowest

### 5.4 Data Fields

| Record | Fields |
|---|---|
| User account | username, email, hashed password |
| Score record | username, game name, score value, date |

---

## 6. Responsive Design Requirements

- The layout must be usable on screen widths from **360px** (mobile) to **1920px** (desktop)

- All 8 pages must apply the colour palette specified in Section 2.3

- All pages must include the website header showing "Fenrir Arena"

---

## 7. File Naming Convention

All page files must follow this pattern:

```
[pagename].html
[pagename].css
[pagename].js
```

**Examples:**

```
index.html
library.html
game.html
login.html
signup.html
profile.html
about.html
contact.html
```

All game files must follow this pattern:

```
games/[gamename].js
```

**Examples:**

```
games/brick-breaker.js
games/snake-classic.js
games/memory-match.js
games/2048-tile-merge.js
games/endless-runner.js
games/sky-dash.js
```

---

## 8. Folder Structure

All files must be submitted using the following folder structure:

```
fenrir-arena/
├── index.html
├── library.html
├── game.html
├── login.html
├── signup.html
├── profile.html
├── about.html
├── contact.html
├── css/
│   └── styles.css
├── games/
│   ├── brick-breaker.js
│   ├── snake-classic.js
│   ├── memory-match.js
│   ├── 2048-tile-merge.js
│   ├── endless-runner.js
│   └── sky-dash.js
├── backend/
│   ├── server.js
│   ├── routes/
│   │   ├── accounts.js
│   │   └── scores.js
│   └── database.sqlite
└── README.md
```

---

## 9. Final Deliverables Checklist

Total page files: **8**

Total game files: **6**

| S.No | Category | File Name | Required Content |
|---|---|---|---|
| 1 | Pages | index.html | Hero banner, tagline, 4 featured games, Browse All Games button |
| 2 | Pages | library.html | Grid of 6 games, category filters (Arcade, Puzzle, Racing), game cards |
| 3 | Pages | game.html | Game canvas, title, description, How to Play section, leaderboard table |
| 4 | Pages | login.html | Email field, password field, Login button, Sign Up link |
| 5 | Pages | signup.html | Username, email, password fields, Create Account button, Login link |
| 6 | Pages | profile.html | Username display, score table per game |
| 7 | Pages | about.html | Description text, tagline verbatim |
| 8 | Pages | contact.html | Name, email, message fields, Send Message button |
| 9 | Games | games/brick-breaker.js | Arcade, paddle controls, score tracking |
| 10 | Games | games/snake-classic.js | Arcade, arrow key controls, score tracking |
| 11 | Games | games/memory-match.js | Puzzle, mouse click controls, score tracking |
| 12 | Games | games/2048-tile-merge.js | Puzzle, arrow key controls, score tracking |
| 13 | Games | games/endless-runner.js | Racing, spacebar controls, score tracking |
| 14 | Games | games/sky-dash.js | Racing, arrow key + spacebar controls, score tracking |
| 15 | Backend | backend/routes/accounts.js | Sign up endpoint, login endpoint |
| 16 | Backend | backend/routes/scores.js | Save score endpoint, leaderboard endpoint |
| 17 | Docs | README.md | Instructions to run the project locally |

---

## 10. Project Reference

| Field | Value |
|---|---|
| Product name | Fenrir Arena |
| Tagline | Play. Compete. Conquer. |
| Total pages | 8 |
| Total games | 6 |
| Backend framework | Node.js with Express |
| Database | SQLite |
| Reference image (provided by client) | reference_image.png |
