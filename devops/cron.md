# How to test cron jobs

Export the cron env:

```
* * * * * env > ~/cronenv
```

then start a shell with the same environment:

```
env - `cat ~/cronenv` /bin/sh
```

Source: [stackoverflow answer 1]

Source: [stackoverflow answer 2]

[stackoverflow answer 1]: http://stackoverflow.com/questions/2135478/how-to-simulate-the-environment-cron-executes-a-script-with
[stackoverflow answer 2]: http://stackoverflow.com/questions/4984725/how-to-test-cron-job
