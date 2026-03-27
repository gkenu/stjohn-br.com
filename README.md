# St. John - stjohn-br.com

## URLs

| URL | What |
|-----|------|
| `stjohn-br.com` | "Em breve" landing page |
| `stjohn-br.com/preview/` | Full site (Fernando review) |

When Fernando approves, move `preview/index.html` to root and delete the coming-soon page.

## Private project files

Research, memory, and export scripts are NOT in this repo. They live locally and are backed up to Google Drive.

| What | Where |
|------|-------|
| Local project | `/Users/kenu/Projects/bmad/projects/stjohn/` |
| Google Drive | `My Drive/Business/StJohn/` |

### Backup command

```bash
rsync -av --exclude='.DS_Store' --exclude='node_modules' \
  "/Users/kenu/Projects/bmad/projects/stjohn/" \
  "/Users/kenu/Library/CloudStorage/GoogleDrive-gkenworthy@gmail.com/My Drive/Business/StJohn/"
```

## DNS Setup (GoDaddy - when ready)

1. GoDaddy DNS for `stjohn-br.com` - add 4 A records (Host: `@`):
   - `185.199.108.153`
   - `185.199.109.153`
   - `185.199.110.153`
   - `185.199.111.153`
2. Add CNAME record: Host: `www`, Value: `gkenu.github.io`
3. GitHub repo Settings > Pages > Custom domain: `stjohn-br.com`
4. Check "Enforce HTTPS" once available

## PDF Export

```bash
cd /Users/kenu/Projects/bmad/projects/stjohn
npm install playwright && npx playwright install chromium
node export-pdf.mjs
```
