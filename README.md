# IET DAVV Campus Quest

A location-based clue hunt for the IET DAVV campus in Indore. Squads solve a quiz,
decode a riddle, walk to the place, and prove they were there with a stamped selfie.

## How a checkpoint works

1. **Quiz.** Answer correctly to break the wax seal on the clue.
2. **Clue.** Read the riddle and work out where it points. Checkpoints stay hidden
   on the map until you clear them. A Cold / Cool / Warm / Hot cue tells you if you
   are getting closer, without showing a distance or a direction.
3. **Arrive.** Tap the arrival button once you are inside the checkpoint's ring.
   Tapping it outside the ring gives a warning. Three warnings void the checkpoint
   and cost 50 points.
4. **Selfie.** Take a selfie inside the ring. It is stamped with the squad name,
   checkpoint, GPS position and time. The place name and a "Did you know?" fact are
   revealed once you clear it.

At the end, the squad gets a rank, a total time and a downloadable passport collage.

## Checkpoints

1. M Block
2. D Block
3. Central Library
4. IET ground
5. Canteen
6. Main Gate

Coordinates, rings (40 m, 50 m at the gate), riddles and quizzes live in
`src/data/defaultCheckpoints.ts`. Coordinates were taken from Google Maps and
satellite view, so walk the route once and adjust them before a real event.

## Two ways to play

- **Live GPS (on campus).** Switch to Live and walk to each place.
- **Demo mode (anywhere).** Drag the dot on the map or use the teleport buttons to
  test the full flow without being on campus.

Demo tools are controlled by `DEMO_TOOLS_ENABLED` in `src/App.tsx`. Set it to
`false` for a real event so players cannot teleport.

## Run locally

```bash
npm install
npm run dev
```

Open http://localhost:3000. The camera and GPS need HTTPS or localhost.

## Notes

- Map tiles come from OpenStreetMap and need an internet connection.
- Game progress, the timer and selfies are saved in the browser's local storage.
- The leaderboard shows sample squads for demo purposes.
- All checks run in the browser, so this is meant for friendly events, not prizes
  that need cheat-proof verification.
