# Score service

The score service of the new infrastructure is by far the most interesting, as it will contain the most new principles.

Rather than score submission processing everything as the score is received, before returning charts to the player, the new score service is aimed to "submit now, process later". This means the score service will rely on other services called "processors" to do the heavy lifting for a lot of the tasks that our previous score services did.

These processors aim to take some stress away from the score service, aswell as allow for better implementation of certain features/tasks which were previously completed on score submission. These are the currently planned processors related to score submission:

- [First place processor](../processors/first.md)
- [User statistics processor](../processors/stats.md)
- [Performance processor](../processors/performance.md)
- [Anticheat processor](../processors/anticheat.md)
- [Leaderboard processor](../processors/leaderboard.md)

There will also be some a system to allow people to easily hook-up their own processors on top of these.