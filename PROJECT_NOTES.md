# Embedded Manager Training Recommender — Project Notes

## What this is

A single-page HTML widget built as a **360Learning demo**. It's a short quiz (6 questions) that recommends one of three manager training programs based on the user's answers.

## Files

| File | Purpose |
|------|---------|
| `index.html` | The entire app — HTML, CSS, and JS in one self-contained file |
| `Build_ Embedded Manager Training Recommender (360Learning Demo).pdf` | Original design/brief |
| `img15733531002518875393-2x.png` | 360Learning logo used in the widget footer |

## Programs the quiz can recommend

| Key | Title | 360Learning URL |
|-----|-------|-----------------|
| `leadershipEssentials` | Leadership Essentials | `.../68ac8b8973d880d8416b5240` |
| `leadingWithoutAuthority` | Leading Without Authority | `.../68ac8b8973d880d8416b523f` |
| `coachingSkills` | Coaching Skills for Managers | `.../68ac8b8973d880d8416b5241` |

## How the quiz logic works

- 6 questions, each answer adds points to one or more of the three program keys
- After all 6 answers, the highest-scoring program is recommended as primary
- If there's a tie, Question 1's answer breaks it
- A secondary "Also consider" link is shown if the runner-up has any points

## Design / brand

- Font: Plus Jakarta Sans (Google Fonts)
- Brand colour: `#5d5fe3` (purple)
- Three screens: Welcome → Question (with back navigation + progress bar) → Results

## Status (as of 2026-04-13)

- Core quiz flow is complete and working
- All three program URLs are live on 360Learning
- No build step — open `index.html` directly in a browser or embed in an iframe

## Possible next steps / things to revisit

- [ ] Add the 360Learning logo image to the welcome card footer (currently at 18% opacity, may need adjusting)
- [ ] Confirm course URLs are correct once published in the customer's 360Learning instance
- [ ] Consider whether a 4th program or additional questions are needed
- [ ] Embed instructions for the customer (iframe snippet, recommended dimensions, etc.)
