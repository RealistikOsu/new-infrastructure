# Leaderboard processor

The leaderboard processor is the final puzzle piece of the [score service](../services/scores.md). Once all other processors have completed, and deemed the score valid, the leaderboard processor is responsible for updating the leaderboard cache for the map. It is at this point that the score will show up on leaderboards ingame.