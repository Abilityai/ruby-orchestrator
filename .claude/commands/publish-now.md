# Publish Now Command

Immediately publish content to specified platforms.

## Usage

```
/publish-now
```

## Workflow

1. Prompt for post content
2. Prompt for target platforms (comma-separated)
3. Optionally prompt for media URLs
4. If media is local file, upload to GoFile first
5. Validate content against platform limits
6. Execute via Blotato posting script
7. Log result to schedule.json with status "published"
8. Report success/failure

## Script Execution

```bash
.claude/skills/blotato-posting/scripts/post.sh "content" "platforms"
```

## Error Handling

- Retry failed platforms up to 3 times
- Log failures for manual review
- Continue with successful platforms
