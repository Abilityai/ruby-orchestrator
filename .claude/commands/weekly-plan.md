# Weekly Plan Command

Monday 9am workflow to plan and schedule the week's content.

## Usage

```
/weekly-plan
```

## Workflow

1. **Analyze Last Week**
   - Query Metricool for performance data
   - Update analytics/weekly_report.json
   - Identify top performers and patterns

2. **Review Available Content**
   - Read content/inventory.json
   - Read strategy/weekly_plan.json from ruby-content
   - Identify content gaps

3. **Create Weekly Schedule**
   - Use batch-scheduler sub-agent
   - Balance hook types (3S+2F)
   - Balance content pillars
   - Assign optimal posting times

4. **Output**
   - Update calendar/schedule.json
   - Update calendar/weekly_plan.json
   - Write event to events/ folder

## Targets

- Twitter: 21 posts/week
- LinkedIn: 7 posts/week
- Instagram: 7 posts/week
- Threads: 14 posts/week
- TikTok: 7 posts/week

## Success Criteria

- All platforms have full week scheduled
- Hook types balanced across week
- No scheduling conflicts
- Optimal times used
