# Cohen's Claude Code Onboarding Page -- Design Document

## Overview
A single-page, fully personalized, gamified onboarding experience for Cohen -- a young, enthusiastic coder getting started with Claude Code CLI, Claude Desktop, and the broader Claude ecosystem. Built as an interactive "cosmic playbook" where each section is a mission to explore.

## Visual Direction: Cosmic/Space Theme
- **Metaphor**: "Unlocking a universe" of AI-powered coding
- **Background**: Deep space gradient (`#0a0a1a` → `#1a0a2e` → `#0a1628`) with animated star particles
- **Cards**: Frosted glass (`rgba(255,255,255,0.05)`) with subtle purple/blue border glow
- **Primary accent**: Electric purple (`#8b5cf6`)
- **Achievement/progress**: Gold (`#f59e0b`)
- **Text**: White (`#f8fafc`) primary, muted (`#94a3b8`) secondary
- **Success**: Emerald (`#10b65a`)

## Tech Stack
- Single HTML file, vanilla CSS + JS (no frameworks)
- CSS custom properties for theming
- localStorage for progress persistence
- CSS animations for particles, glows, transitions
- Font Awesome 7 Pro via kit: `https://kit.fontawesome.com/362a70b2e0.js`

## Page Structure

### Fixed Top Bar
- Progress tracker: "Cohen's Journey -- X/11 Explored"
- Star-field progress bar that fills with gold
- Persists on scroll

### Hero Section (Full Viewport)
- Animated canvas with ~50 drifting star particles
- "Welcome, Cohen" with purple-to-gold gradient text
- "Your journey into AI-powered coding starts here" subtitle
- Pulsing "Begin Your Journey" button with rocket icon
- "11 missions to explore" stat line

### Section Cards (11 total, single column, max-width 800px)

Each card has:
- Collapsed state: icon + title + one-liner + completion badge
- Hover: lift effect + intensified border glow
- Expanded: full content with text, bullets, code snippets, pro-tip callouts
- "Mark as Explored" button triggering gold sparkle animation
- Completed cards get gold border glow + star badge

#### Card Content:

1. **What is Claude Code?** (`fa-wand-magic-sparkles`) -- "Two ways to wield AI power"
   - CLI vs Desktop app comparison, when to use each

2. **Your MAX Subscription** (`fa-crown`) -- "You've got the keys to the kingdom"
   - 5x/20x usage multipliers, extended thinking, priority access, Opus models

3. **Claude Code CLI** (`fa-terminal`) -- "Your command center"
   - Installation, first run, slash commands, file read/write, sample session

4. **Claude Desktop App** (`fa-message-bot`) -- "Your visual thinking partner"
   - Brainstorming, planning, artifacts, when to use vs CLI

5. **Cowork Mode** (`fa-users-gear`) -- "Code together with Claude"
   - Background agent, watches work, suggests improvements, activation guide

6. **Dispatch** (`fa-satellite-dish`) -- "Send out your fleet"
   - Multi-agent orchestration, parallel tasks, newest feature

7. **Essential Plugins** (`fa-puzzle-piece`) -- "Supercharge your setup"
   - Superpowers, Context7, GitHub -- install commands + descriptions

8. **MCPs & Connectors** (`fa-plug-circle-bolt`) -- "Connect Claude to everything"
   - Plain English MCP explanation, key MCPs, installation

9. **Claude in Chrome** (`fa-chrome`) -- "Let Claude see your browser"
   - Browser control, page reading, form filling, testing use cases

10. **Pro Tips** (`fa-stars`) -- "Level up"
    - CLAUDE.md files, prompt engineering, first project ideas

11. **Hidden Final Card** -- Unlocks when all 10 above are completed
    - "You're Ready -- Go Build Something Amazing" with confetti animation

## Interaction Details

### Progress System
- localStorage key: `cohen-journey-progress`
- Top bar updates in real-time
- Star icons appear for each completed section
- 100% completion triggers confetti/star-burst + hidden card reveal

### Animations
- Star particle canvas (lightweight, ~50 particles)
- Card hover lift (translateY -2px)
- Gold sparkle on completion
- Pulsing glow on CTA buttons
- Smooth expand/collapse transitions
- Final confetti celebration

## Personalization
- Cohen's name in hero, progress bar, and scattered throughout content
- Tone: encouraging, exciting, peer-to-peer (not condescending)
- Frame everything as "unlocking power" not "learning basics"
