# Ranked Strength

A competitive video-game style fitness ranking website that tracks exercises and assigns ranks based on performance.

## Overview

Ranked Strength gamifies fitness by implementing a ranking system similar to competitive video games. Users complete workout challenges, track their progress, and climb the ranks from Plastic 5 all the way to Olympic 1.

## Rank Structure

**Ranks (in order):**
- Plastic
- Copper
- Bronze
- Silver
- Gold
- Plat
- Diamond
- Champion
- Olympic

**Divisions:** Each rank has 5 divisions (5, 4, 3, 2, 1)
- Division 5 = Lowest within rank
- Division 1 = Highest within rank
- Everyone starts at **Plastic 5**

## Ranking Rules

1. Users must complete **3 sets** per exercise
2. A rank is earned only if the user reaches the required reps in **ALL 3 sets**
3. Final score = **lowest-performing set**
4. Users cannot qualify based on a single high-performing set

**Example:**
- Set 1: 50 reps
- Set 2: 50 reps
- Set 3: 47 reps
- **Final Score: 47 reps**

## Weight Classes

Separate leaderboards and rankings for:

- **Lightweight:** Under 140 lbs
- **Middleweight:** 140–180 lbs
- **Heavyweight:** Over 180 lbs

Example rank display:
- Lightweight Gold 3
- Middleweight Diamond 2
- Heavyweight Olympic 5

## Exercise Requirements

### Push-Ups
- Plastic 5: 1 push-up per set
- Olympic 1: 150 push-ups per set
- Smooth progression across all ranks and divisions

### Pull-Ups
- Plastic 5: 1 pull-up per set
- Olympic 1: Elite-level endurance (very high reps per set)
- Smooth progression across all ranks and divisions

## Features

✅ User accounts and profiles
✅ Rank badges with icons
✅ Global leaderboards
✅ Weight-class specific leaderboards
✅ Rank progression tracking
✅ Personal records
✅ Exercise history
✅ Statistics dashboard
✅ Progress bars to next rank
✅ Mobile-friendly responsive design
✅ Competitive game-inspired UI

## Tech Stack

- **Frontend:** React, TypeScript, Tailwind CSS
- **Backend:** Node.js/Express, MongoDB
- **Authentication:** JWT
- **Deployment:** Vercel (Frontend), Heroku/AWS (Backend)

## Project Structure

```
ranked-strength/
├── frontend/
│   ├── src/
│   │   ├── components/
│   │   ├── pages/
│   │   ├── services/
│   │   ├── hooks/
│   │   ├── styles/
│   │   └── App.tsx
│   └── package.json
├── backend/
│   ├── src/
│   │   ├── models/
│   │   ├── routes/
│   │   ├── controllers/
│   │   ├── middleware/
│   │   └── server.ts
│   └── package.json
└── README.md
```

## Getting Started

Instructions for setup coming soon.

## License

MIT
