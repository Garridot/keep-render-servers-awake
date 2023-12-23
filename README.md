# Keep Render Servers Awake

This GitHub Actions workflow is designed to send periodic requests to specified Render servers to prevent them from going to sleep due to inactivity.

## Workflow Details

### Servers and Intervals

- **Server 1:**
  - URL: [https://football-player-charts-stats-api.onrender.com/](https://football-player-charts-stats-api.onrender.com/)
  - Interval: Every 25 minutes

- **Server 2:**
  - URL: [https://football-players-charts.onrender.com/](https://football-players-charts.onrender.com/)
  - Interval: Every 30 minutes

- **Server 3:**
  - URL: [https://tomasgarrido.onrender.com/](https://tomasgarrido.onrender.com/)
  - Interval: Every 30 minutes

- **Server 4:**
  - URL: [https://ruins-of-versailles-7rbc.onrender.com/](https://ruins-of-versailles-7rbc.onrender.com/)
  - Interval: Every 30 minutes  

### Workflow Schedule

The workflow is scheduled to run at the specified intervals using cron syntax.

```yaml
on:
  schedule:
    - cron: '*/25 * * * *'  # Run every 25 minutes for Server 1
    - cron: '*/30 * * * *'  # Run every 30 minutes for Server 2
    - cron: '*/30 * * * *'  # Run every 30 minutes for Server 3
    - cron: '*/30 * * * *'  # Run every 30 minutes for Server 4
```