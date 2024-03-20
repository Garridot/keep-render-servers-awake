# Keep Render Servers Awake

This GitHub Actions workflow is designed to send periodic requests to specified Render servers to prevent them from going to sleep due to inactivity.

## Workflow Details

### Servers and Intervals

- **Server 1:**
  - URL: [https://football-player-charts-stats-api.onrender.com/](https://football-player-charts-stats-api.onrender.com/)
  - Interval: Runs the server at 25 minutes past the hour 

- **Server 2:**
  - URL: [https://football-players-charts.onrender.com/](https://football-players-charts.onrender.com/)
  - Interval: Runs the server at 30 minutes past the hour 

- **Server 3:**
  - URL: [https://tomasgarrido.onrender.com/](https://tomasgarrido.onrender.com/)
  - Interval: Runs the server at 30 minutes past the hour 

- **Server 4:**
  - URL: [https://ruins-of-versailles-7rbc.onrender.com/](https://ruins-of-versailles-7rbc.onrender.com/)
  - Interval: Runs the server at 30 minutes past the hour   

### Workflow Schedule

The workflow is scheduled to run at the specified intervals using cron syntax.

```yaml
on:
  schedule:
    - cron: '25 */1 * * *'  # Runs the server at 25 minutes past the hour 
    - cron: '30 */1 * * *'  # Runs the server at 30 minutes past the hour 
    - cron: '30 */1 * * *'  # Runs the server at 30 minutes past the hour 
    - cron: '30 */1 * * *'  # Runs the server at 30 minutes past the hour 
```
