# Ranked Strength - Ranking System Documentation

## Overview

This document outlines the complete ranking system for Ranked Strength, including rank progression, scoring mechanics, and weight class divisions.

## Rank Tiers

| Rank | Level | Progression |
|------|-------|-------------|
| 1 | Plastic | Starting rank for all users |
| 2 | Copper | First progression tier |
| 3 | Bronze | Second progression tier |
| 4 | Silver | Mid-tier rank |
| 5 | Gold | Upper-mid tier |
| 6 | Plat | High-tier rank |
| 7 | Diamond | Elite tier |
| 8 | Champion | Professional tier |
| 9 | Olympic | Highest tier |

## Division System

Each rank has 5 divisions:

```
Rank 5 (Lowest) → Rank 4 → Rank 3 → Rank 2 → Rank 1 (Highest)
```

Progression path:
```
Plastic 5 → Plastic 4 → Plastic 3 → Plastic 2 → Plastic 1 → Copper 5 → ... → Olympic 1
```

Total ranks: 9 × 5 = **45 unique rank/division combinations**

## Push-Up Progression

Smooth progression from Plastic 5 (1 rep) to Olympic 1 (150 reps).

### Calculation Formula

For push-ups, we calculate the required reps for each rank/division:

```
rank_index = (rank - 1) × 5 + (5 - division) + 1
required_reps = 1 + ((rank_index - 1) / 44) × 149
```

This creates a smooth progression:

### Push-Up Requirements by Rank

| Rank | Div 5 | Div 4 | Div 3 | Div 2 | Div 1 |
|------|-------|-------|-------|-------|-------|
| Plastic | 1 | 5 | 9 | 13 | 17 |
| Copper | 21 | 26 | 30 | 34 | 38 |
| Bronze | 42 | 46 | 51 | 55 | 59 |
| Silver | 63 | 67 | 72 | 76 | 80 |
| Gold | 84 | 88 | 93 | 97 | 101 |
| Plat | 105 | 109 | 114 | 118 | 122 |
| Diamond | 126 | 130 | 135 | 139 | 143 |
| Champion | 147 | 147 | 148 | 149 | 149 |
| Olympic | 150 | 150 | 150 | 150 | 150 |

## Pull-Up Progression

Smooth progression from Plastic 5 (1 rep) to Olympic 1 (elite-level high reps).

### Pull-Up Requirements by Rank

For elite pull-up standards, we cap at 50 reps for Olympic 1:

| Rank | Div 5 | Div 4 | Div 3 | Div 2 | Div 1 |
|------|-------|-------|-------|-------|-------|
| Plastic | 1 | 2 | 3 | 4 | 6 |
| Copper | 8 | 9 | 11 | 12 | 14 |
| Bronze | 16 | 17 | 19 | 21 | 22 |
| Silver | 24 | 26 | 27 | 29 | 31 |
| Gold | 32 | 34 | 36 | 37 | 39 |
| Plat | 41 | 42 | 44 | 46 | 47 |
| Diamond | 49 | 50 | 50 | 50 | 50 |
| Champion | 50 | 50 | 50 | 50 | 50 |
| Olympic | 50 | 50 | 50 | 50 | 50 |

## Scoring Mechanics

### Three-Set System

Users complete 3 sets per exercise attempt:

1. **Set 1:** First attempt
2. **Set 2:** Second attempt
3. **Set 3:** Third attempt

### Final Score Calculation

**Final Score = Minimum(Set 1, Set 2, Set 3)**

This ensures users cannot qualify for a rank based on luck or a single good set.

### Rank Qualification

- User qualifies for a rank if their **final score ≥ required reps for that rank**
- User automatically advances to the lowest uncompleted rank
- Users must exceed current rank requirements to advance to next division/rank

### Personal Records (PRs)

- Track best score across all sets for each exercise
- Update when user exceeds previous best minimum score
- Display in user profile and statistics dashboard

## Weight Classes

### Class Definitions

| Weight Class | Bodyweight Range |
|---|---|
| Lightweight | < 140 lbs |
| Middleweight | 140 - 180 lbs |
| Heavyweight | > 180 lbs |

### Weight Class Implementation

- Users enter bodyweight during signup
- Users can update weight in profile settings
- Separate ranking calculations for each weight class
- User displays all three ranks: "Lightweight Gold 3 | Middleweight Diamond 2 | Heavyweight Olympic 5"
- Global and weight-class specific leaderboards

### Leaderboard Types

1. **Global Leaderboard:** All users ranked together
2. **Weight-Class Leaderboards:** Separate rankings for each weight class
3. **Exercise-Specific Leaderboards:** Best performance in push-ups or pull-ups
4. **Time-Based Leaderboards:** Week, Month, All-Time

## Advancement Example

**Scenario: User attempts Push-Ups at Plastic 5 (requires 1 rep)**

```
Attempt 1:
- Set 1: 15 reps
- Set 2: 14 reps
- Set 3: 13 reps
- Final Score: 13 reps ✓ Qualifies for Plastic 5

Attempt 2 (later):
- Set 1: 20 reps
- Set 2: 18 reps
- Set 3: 16 reps
- Final Score: 16 reps ✓ Qualifies for Plastic 4

Attempt 3 (later):
- Set 1: 25 reps
- Set 2: 24 reps
- Set 3: 22 reps
- Final Score: 22 reps ✓ Qualifies for Plastic 3

Current Rank: Plastic 3
Progress to Plastic 2: Needs 13 reps (next threshold)
Distance to Olympic 1: 150 reps (127 reps to go)
```

## Rank Icons and Badges

Each rank will have:
- Unique icon/badge design
- Color coding by tier
- Division number display
- Weight class indicator

## Statistics Tracked

- Total attempts per exercise
- Average score per exercise
- Personal record per exercise
- Current rank in each weight class
- Rank history/progression timeline
- Consistency metrics (variance between sets)
- Time to reach each rank
