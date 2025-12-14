# Daily Routine Command

Daily health check and publishing verification.

## Usage

```
/daily-routine
```

## Workflow

1. **System Health**
   - Update orchestrator heartbeat
   - Check other agents' heartbeats
   - Verify API connectivity

2. **Publishing Check**
   - Review posts scheduled for today
   - Verify media URLs still valid
   - Re-upload expired GoFile URLs if needed

3. **Performance Review**
   - Check yesterday's post performance
   - Note any failed posts for retry

4. **Report**
   - Update monitoring/health_status.json
   - Log any alerts
   - Summarize day's schedule

## Output

Brief summary of:
- System health status
- Posts scheduled for today
- Any issues requiring attention
