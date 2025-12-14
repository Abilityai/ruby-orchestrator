# Schedule Post Command

Schedule a single post to specified platforms at a given time.

## Usage

```
/schedule-post
```

## Workflow

1. Prompt for post content
2. Prompt for target platforms (comma-separated)
3. Prompt for schedule time (ISO 8601 format)
4. Optionally prompt for media URLs
5. Validate content against platform limits
6. Add to schedule.json
7. Confirm scheduling

## Platform Limits

- Twitter: 280 chars
- Threads: 500 chars
- Instagram: 2,200 chars (requires media)
- LinkedIn: 3,000 chars

## Example

```
Content: AI agents are the future of work. Here's why...
Platforms: twitter, linkedin
Time: 2025-01-15T09:00:00Z
Media: (optional)
```

Adds entry to `/home/developer/shared-out/calendar/schedule.json` with status "scheduled".
