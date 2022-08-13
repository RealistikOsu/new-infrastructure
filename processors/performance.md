# Performance processor

The performance processor will constantly listen for scores and calculate their PP. This not only allows for osu!lazer to be used for calculations, ensuring stability and up-to-date performance systems, but also makes recalculating scores en masse incredibly easy.

The [score service](../services/scores.md) will initially wait a timeout for this processor when a new score is submitted to attempt to display a score's pp to the user immediately, however depending on load the processor may not be able to calculate in time in which case the user may have to wait a few minutes.

To aid the ease of performance calculation, the database will hold the pp for scores in a separate table from the score data. This allows for efficient updating without locking all score data.