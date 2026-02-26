# The Barnes Files - Interactive Timeline

Hosted timeline for [belligerentbeavs.com](https://belligerentbeavs.com).

## Setup

1. Create a new repo on GitHub named `barnes-files-timeline`
2. Push this folder to it
3. Enable GitHub Pages: **Settings > Pages > Source: Deploy from branch > main / (root)**
4. Wait ~60 seconds, your timeline lives at `https://YOUR_USERNAME.github.io/barnes-files-timeline/`
5. In Squarespace, paste the contents of `SQUARESPACE_EMBED.html` into a Code Block in your blog post (update the username in the iframe src)

## Structure

```
index.html                  # Timeline (41KB)
images/
  bpse_contract_fee_structure.png    # Contract exhibit (570KB)  
  sole_source_procurement_memo.png   # CPO memo exhibit (575KB)
SQUARESPACE_EMBED.html      # Paste this into Squarespace
```

## Why this approach

Squarespace Code Blocks parse HTML inline, so a 1.6MB file with base64 images is brutal on rendering. This splits images out as separate lazy-loaded files and loads the whole timeline in an iframe, so Squarespace's CSS/JS doesn't interfere and images cache independently.
