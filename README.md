# probe
Haas VF-4 TRT probing via post processor
PROJECT: Haas VF-4 TRT probing via post processor

GOAL:
Post-driven probing system using Renishaw Inspection Plus macros.
Programmer chooses which features are probed before posting.
Auto-correct tool wear and/or work offsets.

MACHINE:
- Haas VF-4 with TRT rotary
- WIPS / Renishaw Inspection Plus installed

FEATURES TO SUPPORT:
1. Bore / boss diameter (auto tool wear correction)
2. Pocket / slot width + length (pass/fail initially)
3. Z datum / face (work offset update)

SELECTION METHOD:
- Marker operations in Mastercam
- Identified by operation name prefix: PRB_
- Parameters stored in Misc Integers/Reals

POST RESPONSIBILITIES:
- Detect PRB_ operations
- Output safe probe positioning
- Call appropriate Renishaw macros (9811 / 9812 / 9814)
- Apply correction logic
- Restore machine state

NON-GOALS:
- No GUI interaction
- No geometry analysis
- No toolpath creation
