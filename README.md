<img width="1280" height="640" alt="git (1)" src="https://github.com/user-attachments/assets/8920b256-2ba8-4988-b824-5351134eb4bd" />



# Trust_Issues.exe 🎯


## Basic Details
### Team Name: Code Duo


### Team Members
- Team Lead: Laura Saju - Viswajyothi College Of Engineering And Technology
- Member 2: Angel Antony - Viswajyothi College Of Engineering And Technology

### Project Description
Trust issues.exe is a chaotic prank web game where an impossible CAPTCHA, a hum-powered download, and Flappy Bird-style challenge spiral into a fake-hack jump scare

### The Problem (that doesn't exist)
Solving the urgent crisis of people who pass CAPTCHAs too easily and download bird games without proving they can hum under pressure.

### The Solution (that nobody asked for)
An aggressively judgmental CAPTCHA that makes you hum to unlock Flappy Bird—then “rewards” success with a fake-hack jump scare.

## Technical Details
### Technologies/Components Used
For Software:
- HTML5
- CSS3
- Vanilla JavaScript
- Google Fonts

### Implementation
For Software: Trust_Issues.exe is a single self-contained HTML/CSS/JavaScript file with no build step or framework — a state machine toggles between stages (intro, login, CAPTCHA, download, game, cutscene, reveal) using CSS class swaps rather than routing. All audio (background music, jump-scare sounds, UI blips) is synthesized live via the Web Audio API using raw oscillators, not pre-recorded files. The Flappy Bird game runs on Canvas 2D with manual physics (gravity, flap impulse, AABB collision), and its background music volume is recalculated every frame from the bird's height. The download screen uses `getUserMedia` and an `AnalyserNode` to detect humming by RMS volume, resetting instantly on silence. The one real backend dependency is a shared prank counter, implemented as an atomic Postgres RPC function on Supabase, called via `supabase-js`, with graceful fallbacks to Claude's artifact storage or an in-memory counter if Supabase isn't configured — so the app never breaks regardless of what's wired up.

# Installation
npm install -g vercel

# Run
VS code Live Server

### Project Documentation
For Software: Trust_Issues.exe is a browser-based prank web application that guides visitors through a fake login, a rigged CAPTCHA that rejects every answer with escalating insults, a microphone-activated download bar, and a Flappy Bird minigame whose volume tracks the bird's height — before ending in a scripted glitch/blackout/jump-scare sequence and a reveal screen showing how many people have been pranked. It's built as a single dependency-free HTML file (no framework, no build step) using vanilla JavaScript, Canvas 2D for the game, and the Web Audio API for all synthesized sound effects and music; the only external service is Supabase, which powers a shared, atomically-incremented prank counter via a Postgres RPC function, with automatic fallbacks so the app degrades gracefully if it's not configured. It requires microphone permission for the download stage and a secure context (`localhost` or HTTPS) to run properly, and can be deployed to any static host such as Vercel with zero configuration.

# Screenshots (Add at least 3)
[Project title interface] (image-2.png)
"Trust_Issues.exe" title screen — the app's intro reveal, after its fake system-crash buildup settles into the final title card. The [ START ] button blinks amber/dark at ~2.5 times per second to draw the eye, and clicking it fades this screen out to reveal the login page underneath.

[Login Interface] (image-1.png)
Login screen — the retro Windows-98-styled entry point of the app. Any username and password are accepted; there's no real authentication at all. The "Remember me (we won't)" checkbox is a small joke rather than a functional option, and clicking "LOG IN →" always proceeds straight to the next stage regardless of what was entered.

[CAPTCHA verification] (image-3.png)
"Prove It" image CAPTCHA — the question changes each attempt (here: "Select all squares with trees" instead of the traffic-light example). The user has actually selected all three correct tiles, but the CAPTCHA is rigged to reject the answer regardless — shown here on attempt 2 of 4, paired with one of the randomized meaner insults that vary each time rather than repeating the same line.

# Diagrams
[Once the game ends — either by hitting a pipe or the hard 7-second timer — control passes into the payoff sequence: the cutscene, the shared prank counter, and the final reveal.] (image-5.png)
[Two things worth calling out that the diagrams simplify: the CAPTCHA stage isn't a straight pass-through — it loops through up to 4 rigged attempts before letting the user continue regardless of what they picked. And the game's ending is a race between two conditions, whichever fires first: a pipe collision or the 7-second hard timer — either one triggers the same cutscene.] (image-4.png)

# Video
[<video controls src="Screen Recording 2026-09-06 072944.mp4" title="Title"></video>] 
This self-contained web app demonstrates a playful, intentionally absurd digital prank experience: users pass through a mock login, randomized hostile CAPTCHA challenges, a microphone-powered “download,” and a Flappy Bird-style game before encountering a simulated display blackout, fake system message, and randomized jump scare. It showcases HTML, CSS, Canvas, Web Audio, microphone input, local storage, animation, and browser-based interaction in one standalone file.

# Additional Demos
[C:/Users/Laura/Documents/Codex/2026-09-05/create-a-webapp-called-trust-issues/outputs/trust-issues-exe/index.html]

## Team Contributions
- Laura Saju: Frontend
- Angel Antony: Backend

---
Made with ❤️ at TinkerHub Useless Projects 

![Static Badge](https://img.shields.io/badge/TinkerHub-24?color=%23000000&link=https%3A%2F%2Fwww.tinkerhub.org%2F)
![Static Badge](https://img.shields.io/badge/UselessProjects--26-26?link=https%3A%2F%2Ftinkerhub.org%2Fevents%2F1M8ORET9A1%2Fuseless-projects-3.0)



