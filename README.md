# The Barnes Files — Interactive Timeline

Hosted timeline for [belligerentbeavs.com](https://belligerentbeavs.com).

## Quick Start

1. Clone/download this repo
2. Drop your renamed PDFs into the `docs/` directories (see `docs/README.md` for the filename mapping)
3. Create `docs/PRR_2025-396_All_Records.zip` containing all PDFs
4. Push to GitHub
5. Enable GitHub Pages: **Settings > Pages > Source: Deploy from branch > main / (root)**
6. Wait ~60 seconds — your timeline lives at `https://YOUR_USERNAME.github.io/barnes-files-timeline/`
7. In Squarespace, paste `SQUARESPACE_EMBED.html` into a Code Block (update the username)

## Structure

```
index.html                              # Timeline (45KB)
images/
  bpse_contract_fee_structure.png       # Contract exhibit screenshot
  sole_source_procurement_memo.png      # CPO memo exhibit screenshot
docs/
  README.md                             # Filename mapping guide
  PRR_2025-396_All_Records.zip          # Bulk download (you create this)
  batch-1/
    BPSE_Oregon_State_Services_Agreement.pdf
    CPO_Sole_Source_Approval.pdf
  batch-3/
    Barnes_Bjornstad_Correspondence.pdf
    Ulrey_Barnes_NCAA_Concern.pdf
    Kyle_Ulrey_BSP_Request.pdf
  batch-4/
    Blaylock_SMS_Records_Redacted.pdf
SQUARESPACE_EMBED.html                  # Paste into Squarespace
```

## How Links Work

Every "View source document" link in the timeline points to `docs/batch-N/filename.pdf`. GitHub Pages serves these as static files, so they load fast and are permanently linkable. The "DOWNLOAD ALL RECORDS" CTA points to `docs/PRR_2025-396_All_Records.zip`.

## Why GitHub Pages

Squarespace Code Blocks can't handle large inline HTML. This approach splits images and PDFs into separate cacheable files, loads the timeline in an iframe, and keeps all source documents under version control.
