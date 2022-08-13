# Leaderboard service

Rather than cramping all web routes into one service (e.g LETS, USSR), they will be split into multiple services, with the leaderboard service being one of them.

## Efficient, stateless cache

A large part of server overhead is constantly fetching scores to display on leaderboards in-game. With a cache stored in Redis, we can prevent the database getting slow and inefficient as much as possible. Cache should be stored initially for 24 hours, with that 24 hours resetting each time the leaderboard is requested or receives a new score.