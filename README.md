# scheduled-action-demo

- The shortest interval you can run scheduled workflows is once every 5 minutes, see <https://docs.github.com/en/actions/using-workflows/events-that-trigger-workflows#schedule>

```shell
on:
  schedule:
    - cron: '*/5 * * * *'
```
