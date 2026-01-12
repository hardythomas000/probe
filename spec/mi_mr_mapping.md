MI1 = Feature type
  0 = Not a probe feature
  1 = Bore / Boss (diameter)
  2 = Pocket / Slot (width + length)
  3 = Face / Z datum

MI2 = Correction mode
  0 = Measure only (alarm if out)
  1 = Auto tool wear correction
  2 = Update work offset

MI3 = Target number
  If MI2 = 1 → Tool wear number (D offset)
  If MI2 = 2 → Work offset number (e.g. 54, 55)

MI4 = Probe timing
  0 = Before finishing operations
  1 = After finishing operations

MI5 = Probe orientation mode
  0 = Use current plane
  1 = Force safe probe plane (recommended)

  ---------------------------------------------
  
MR — Misc Reals (geometry & tolerance)

MR1 = Nominal size (primary)
  Bore/Boss → Diameter
  Pocket/Slot → Width
  Face → unused

MR2 = Nominal size (secondary)
  Pocket/Slot → Length
  Others → unused

MR3 = Tolerance (+/-)
  Applies to all feature types

MR4 = Z approach height
  Safe distance above feature before probing

MR5 = Measure depth
  Z depth at which probing occurs (negative down)
