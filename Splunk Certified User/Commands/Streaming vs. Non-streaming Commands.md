# Streaming vs. Non-streaming commands

### Transforming Commands
Operate on the entire result set of data

| stats
| timechart 
| chart 
| top 
| rare

### Streaming Commands
- Centralized
- Distributable

### Centralized Streaming Commands
- Stateful streaming commands
Incoming results based upon how they came to them
- | transaction
- | streamstats

### Distributable Streaming Commands
Order events are returned in doesn't matter

| rename
| eval 
| fields 
| regex


