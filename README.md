# Star Catcher

A retro arcade game styled like an 80s monochrome CRT. Catch falling stars before they hit the ground, build combos for bonus points, and make a wish on each star you catch. Miss too many and it's game over.

Built as a single HTML5 canvas file, wrapped with Capacitor for iOS deployment.

## Play

Open `index.html` in any browser. Use arrow keys or touch to move.

## iOS Build

Requires Node.js and Xcode.

```bash
npm install
cp index.html www/ && npx cap sync ios
npx cap open ios
```

Then build and run from Xcode (Cmd+R).

## Stack

- Vanilla HTML/CSS/JS (no frameworks, no bundler)
- HTML5 Canvas with pixel art sprites
- Capacitor 8 for native iOS wrapper
