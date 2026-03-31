# Development Timeline Estimate: Star Catcher 1.0

## Project Scope

Single-file HTML5 canvas game (1,461 lines) with Capacitor iOS wrapper. 80s monochrome CRT aesthetic, pixel art sprites, Web Audio API sound design, Supabase backend for wish persistence.

## System Breakdown

| System | Complexity | Est. Effort |
|---|---|---|
| Rendering pipeline (dual-canvas, pixel scaling, CRT effect) | Medium | 2-3 days |
| Player movement (touch + keyboard, normal + space mode) | Low-Medium | 1-2 days |
| Star spawning & catching (3 sizes, 3 types, reachability logic) | Medium | 2-3 days |
| Space mode (triggered at 44 catches, 2D movement, music switch) | Medium | 1-2 days |
| Obstacles — planets (4 sizes, 6 palettes), comets (trails, shattering), debris | High | 3-4 days |
| Particle system (catch bursts, comet trails, collision effects) | Medium | 1-2 days |
| Custom bitmap font (3x5 pixel glyphs, A-Z + 0-9) | Low | 0.5 day |
| Pixel art sprites (player, stars, planets, comets, debris, life indicator) | Medium | 2-3 days |
| Audio — Web Audio API synth sounds, combo system with reverb, music loading | High | 3-4 days |
| Game loop & difficulty curve (sigmoid ramp, spawn intervals) | Medium | 1-2 days |
| UI overlay system (start, stats, wish input, leaderboard, starfield bg) | Medium | 2-3 days |
| Supabase backend (wish save/load, REST API) | Low | 0.5-1 day |
| Wish classification (23 theme categories, keyword matching) | Low-Medium | 1 day |
| Capacitor iOS wrapper (config, safe area handling, notch detection) | Low-Medium | 1-2 days |
| CSS/styling (CRT scanlines, retro buttons, Press Start 2P font) | Low | 1 day |
| Playtesting & tuning (difficulty curve, hitboxes, spawn balance, combo windows) | High | 3-5 days |

## Summary

| Phase | Estimate |
|---|---|
| Raw development | ~25-35 person-days |
| Design & art direction | ~5-8 days |
| Playtesting & polish | ~5-8 days |
| iOS deployment (certificates, App Store assets, review) | ~2-3 days |
| **Total** | **~37-54 person-days** |

## For a Small Team (2-3 devs)

- **Optimistic**: 3-4 weeks (experienced game devs, clear vision from day one, minimal iteration)
- **Realistic**: 5-7 weeks (some iteration on feel/balance, learning Capacitor, App Store process)
- **Conservative**: 8-10 weeks (newer to canvas games or needs significant design exploration)

## Accelerating Factors

- Zero dependencies (no framework, no build tools, no bundler)
- Single-file architecture eliminates all module/build complexity
- Monochrome palette eliminates most art pipeline work
- Supabase handles the entire backend with ~30 lines of code

## Risk Factors

- The audio system is surprisingly sophisticated (convolver reverb, combo-driven wet/dry mix, harmonic overtones) — 3-4 days of specialized work
- The spawn reachability algorithm required careful game design iteration
- Planet/comet/debris collision matrix is combinatorially complex (planet-planet, comet-planet, comet-player, debris-player)
- Playtesting and tuning difficulty curves is inherently time-consuming and iterative

## Conclusion

A competent 2-person team could ship this in about 5-6 weeks. The code is clean and the scope is well-contained. The hardest parts are the audio design and gameplay tuning, not the engineering.
