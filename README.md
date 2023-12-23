# Keep Render Servers Awake

This GitHub Actions workflow is designed to send periodic requests to specified Render servers to prevent them from going to sleep due to inactivity.

## Workflow Details

### Servers and Intervals

- **Server 1:**
  - URL: [https://football-player-charts-stats-api.onrender.com/](https://football-player-charts-stats-api.onrender.com/)
  - Interval: Every 30 minutes

- **Server 2:**
  - URL: [https://football-players-charts.onrender.com/](https://football-players-charts.onrender.com/)
  - Interval: Every 25 minutes

### Workflow Schedule

The workflow is scheduled to run at the specified intervals using cron syntax.

```yaml
on:
  schedule:
    - cron: '*/30 * * * *'  # Run every 30 minutes for Server 1
    - cron: '*/15 * * * *'  # Run every 15 minutes for Server 2
```