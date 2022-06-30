# | transaction Command

- Group events that share one or more fields
	- Group events on values from _field_
	- Group events based on shared values from _field-list_
- Determine event grouping behavior using _options_:
	- Ranges of time: _maxspan, maxpause_
	- Maximum number of events in a transaction: _maxevents_
	- Text contained in the first/last events


>[!IMPORTANT]
>REQUIRES events to be in REVERSE CHRONOLOGICAL ORDER
 
 ### Considerations
 
 - the transaction command is resource intensive

- Only use transaction if you:
	- Need to group events on values from multiple fields
	- Need to define event grouping on start/end values or segment time
	- Want to keep raw data associated with each event
- Otherwise, use stats command
	- Faster and more efficient
	- Can perform calculations
	- Can group events based on a single field value (e.g. by src_ip)
