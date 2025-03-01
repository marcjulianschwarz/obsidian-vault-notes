```bash
find / -type f -size +200M -exec du -h {} + 2>/dev/null | sort -r -h
```