# OCES Car Rider Board

A QR-based dismissal board for the car rider line at Oglethorpe County
Elementary School. Teachers scan each car's tag with an iPad as they work
down the lane; student names populate a display board inside, organized into
waves that match the numbered cones outside.

**Live demo:** https://ssynan-oss.github.io/OCES-Car-riders/

## How it works
- Teachers scan cars in lane order; the board holds a running queue per row.
- The queue is windowed into three tiers: **At the cones** (loading now),
  **On deck** (next wave, being called), and a **buffer** of cars scanned
  further ahead.
- Advancing a row drops the loaded wave and slides everything up — no pause
  in calling names, no blank board between waves.
- Siblings share one cone. Cars without a tag can be added by name.

## Status
This is a single-screen prototype for demonstrating the workflow. The live
version — two iPads writing to the board in real time — runs on a shared
backend (Airtable) and uses QR tags encoding a family ID rather than names.
Those pieces come next.
