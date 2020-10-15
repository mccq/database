You can use the `schedule` command to run a function after a given time.

It has the following syntax:
```
schedule function <function> <time> [append|replace]
```

Examples of `<time>` are
- `1t` 1 tick
- `4s` 4 seconds
- `3d` 3 in-game days
- `0.5s` 0.5 seconds or 10 ticks

The default behavior is to `replace` any previous scheduled functions with the same name.

Keep in mind that scheduling a function will lose the execution context!
