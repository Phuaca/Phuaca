# Phua Cheng Ann

I'm a Computer Science student at DigiPen in Singapore. I build Android apps and games using C++, Kotlin and C#.

## Project case studies

- [Runi](#runi) is my main project, an Android app for racing against recorded runs.
- [BitBlast](#bitblast) shows my work on procedural terrain and multiplayer sync in C++.
- [A Quiet Shift](#a-quiet-shift) is a Unity puzzle game we built in seven days.

### Runi

*Ongoing university team project | Android, C++, Kotlin*

Runi lets a runner race against their personal best, a previous run and a shared recording. I built the C++ engine that processes Global Positioning System (GPS) data and the Kotlin controls for choosing recordings. I connected them through the Java Native Interface (JNI) and reused one set of live tracking data to compare progress against all three recordings.

I replayed 12 recordings to check tracking. During upload testing, late GPS updates put recording timestamps out of order and caused the server to reject a run. I kept the recording clock from moving backward, preserved the original GPS sample times and added a regression test. All seven Android tracking tests passed, and the server verified a new upload.

### BitBlast

*University team project | C++, DigiPen Alpha Engine*

BitBlast is a two-player artillery game. The terrain needed to vary between matches while giving both tanks stable ground to start on. Both players also needed to see the same terrain changes after an explosion.

I built a terrain generator using a random walk with limits on slope and height. I worked with teammates to place tanks on relatively flat starting ground, added destructible terrain and helped send each explosion's position and radius to the other client so it could reproduce the crater. We tested several generated maps and confirmed both tanks could spawn safely, move, aim and fire.

### A Quiet Shift

*Gameplay programmer | Unity, C# | Century Games Game Jam 2026*

Our team had seven days to deliver a playable first-person horror puzzle game. I built a raycast interaction system with a shared `IInteractable` interface for doors, switches and other puzzle objects. I also implemented the circuit breaker puzzle and an inspection mode for clues.

During testing, pressing E did nothing on the TV or main circuit breaker. Both objects responded to clicks, so I traced the issue to the raycast detection path, which missed both. I updated the player interaction code to detect them and show a contextual prompt. Both objects then responded to E. The team released a playable Windows build by the jam deadline.

[View the game and download the Windows build](https://jordan-yeo.itch.io/a-quiet-shift)

## Relivio browser demo

Relivio is our HackRift 2025 prototype for helping vendors list surplus food for pickup. I built browser photo capture for a recorded local demo and verified that a captured photo appeared in the vendor's listing.

[Open the public team prototype](https://relivio.netlify.app/) to browse sample listings in a feed or map.

## PracticeSG

PracticeSG is a team web app for practising everyday digital tasks in Singapore. It simulates services such as Singpass and PayNow and includes a scam awareness quiz. I built the text-to-speech feature using the browser's Web Speech API so users could hear the instructions, and I built parts of the interface.

[View the PracticeSG team repository](https://github.com/jordanyeo2001/PracticeSG)

## Contact

[Connect with me on LinkedIn](https://www.linkedin.com/in/cheng-ann-phua/)
