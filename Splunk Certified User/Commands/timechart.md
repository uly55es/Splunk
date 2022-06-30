# | timechart Command

Performs statistical aggregations against time and returns a time series chart where __time__ is always the X-axis

* EXAMPLE
```spl
| timechart >stats-func<(<field>) by <split-by-field> [span=<int><timescale>] [limit=<int>]
```

stats-func(field) applies a funciton to a single field and populates the Y-axis
- if using the count function, a field does not need to be specified


* NOTE
> timechart only supports a single additional split



can use:
- span
	- timechart buckets the value of the time field based on time range if no span argument is specified
		- a. Last 60 minutes defaults to span=1m
		- b. Last 24 hours defaults to spam=30m
- limit
