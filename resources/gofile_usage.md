# GoFile Integration Guide

## Overview

GoFile is the temporary media hosting solution for social media posts. It provides:

- **Unlimited file size** (free tier)
- **10-30 day auto-deletion** (perfect for scheduled posts)
- **Simple API** with shareable URLs
- **No manual cleanup needed**

## Quick Start

### Upload a File

```bash
scripts/gofile_upload.sh /path/to/video.mp4
# Returns: https://gofile.io/d/XXXXXX
```

### Use with Blotato

```bash
# Upload to GoFile first
URL=$(scripts/gofile_upload.sh /path/to/video.mp4)

# Then use URL with Blotato posting
.claude/skills/blotato-posting/scripts/post.sh "Caption" "twitter,instagram" "" "$URL"
```

## Typical Workflow

1. **Generate/download video** to local file
2. **Upload to GoFile** using the script
3. **Use URL with Blotato** for posting
4. **GoFile auto-deletes** in 10-30 days (no action needed)

## Best Practices

1. **Upload immediately before posting/scheduling**
   - Don't upload weeks in advance
   - GoFile is for active content, not long-term storage

2. **Track URLs in registry**
   - Update `/home/developer/shared-out/media/url_registry.json`
   - Include expiration dates (30 days from upload)

3. **Use URLs within days**
   - Perfect for scheduled posts (next 1-7 days)
   - Don't rely on links older than 30 days

4. **No cleanup needed**
   - Files auto-delete
   - Don't worry about manual removal

## Troubleshooting

### Upload Fails
- Check credentials in .env (GOFILE_API_TOKEN, GOFILE_ROOT_FOLDER)
- Verify file exists and is readable
- Check internet connectivity

### Slow Upload
- Large files (GB+) take time
- Server selection is automatic
- Add progress flag if needed: `curl -v`

## Cost

**GoFile Free Tier:**
- Storage: Unlimited
- File size: Unlimited
- Retention: 10-30 days
- Uploads: 100,000 items
- Cost: $0/month

## When to Use vs. Not Use

**Use GoFile for:**
- Video posts to social media
- Image carousels
- Any media for scheduled posts
- Temporary sharing links

**Don't use GoFile for:**
- Long-term storage (use Google Drive)
- Permanent archives
- Content older than 30 days
