# date and time

## date

```
date(question, aid='enter a date', **kwargs)
```

Asks user to enter a date using the formar yyyy-mm-dd. Using other format like yyyy-mm-d (example 2026-12-5) or yyyy-mm (example 2000-05) results in an error.

Example

```
>>> import pyask
>>> pyask.date("What is the date")
What is the date? (enter a date) [] 2026-12-05
datetime.date(2026, 12, 5)
```

# Original project
to submit a [Pyask](https://github.com/tmward/pyask/)
