# z-score

Calculate Z Score and related percentile/observation values based on the Z score table from CollegeBoard. To find the same table, view the third page of
[the AP Statistics formula sheet and tables](https://apcentral.collegeboard.org/pdf/statistics-formula-sheet-and-tables-2020.pdf).

# Functions

Functions are not ordered by usefulness. For example, so read through or gloss over all functions to look for what you need. Keep in mind that all percentiles/percentages are represented by a float between 0 and 1. Values usually are rounded to 4 decimal places.

While unrelated, don't forget to remember if the value you are trying to determine is below or above the cutoff range! If a question asks you to find the percentage above a certain observation, you'll have to find the percentile of that observation, and then subtract it from 1. The program and functions do not do this for you!

### `z_score_from_percentile(percentile) -> float`

Get the Z score from a given percentile using the Z score table. Percentiles must be between 0.0002 and 0.9998. Returns the Z score as a float.

### `observation_from_percentile(percentile, mean: float, sd: float) -> float`

Get an observation value from a given percentile. Percentiles must be between 0.0002 and 0.9998. Mean and standard deviation must also be provided. Returns the observation value as a float.

### `observation_from_z_score(z_score: float, mean: float, sd: float) -> float`

Get the observation value from a given Z score. Percentiles must be between 0.0002 and 0.9998. Mean and standard deviation must also be provided. Returns the observation as a float.

### `percentile_from_z_score(z_score: float) -> float`

Get the percentile from a Z score using the Z score table. Returns the percentile as a float between 0 and 1.

### `z_score_from_observation(obsv: float, mean: float, sd: float) -> float`

Get the Z score from an observation. Mean and standard deviation must also be provided. Returns the Z score as a float.

### `percentile_from_observation(obsv: float, mean: float, sd: float) -> float`

Get the percentile from an observation. Mean and standard deviation must also be provided. Returns the percentile as a float between 0 and 1.

### `percentage_between_observations(lower_obsv: float, higher_obsv: float, mean: float, sd: float) -> float`

Get the percentage between two observations. Mean and standard deviation must also be provided. Returns a percentage as a float between 0 and 1.

### `percentage_between_z_scores(lower_z_score: float, higher_z_score: float) -> float`

Get the percentage between two Z scores. Returns a percentage as a float between 0 and 1.

### `quartiles(mean: float, sd: float) -> tuple`

Get the 5 number summary (minimum, quartile 1, median, quartile 3, maximum) and interquartile range of the given mean and standard deviation. Returned tuple has values in the order of `(min_value, q1, median, q3, max_value, iqr)`.
