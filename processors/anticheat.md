# Anticheat processor

The anticheat processor will listen for new scores and attempt to find cheats in various methods. One method will be replay postprocessing, where it will check that a replay has valid UR and frametime (and in the future, possibly check for replay botting). The processor will also handle pp caps, and check for other mysterious behaviour about the score which warrant a restriction on the user.

The exact implementation details of this are unknown, but are likely to be expanded on later.