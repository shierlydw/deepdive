# What to upload

## Add / replace

| File | Goes to |
| --- | --- |
| `index.html` | repo root (replace the existing one) |
| `assets/images/lr_img_14.webp` | `assets/images/` (new file) |
| `assets/images/lr_img_22.webp` | `assets/images/` (new file) |
| `assets/images/lr_img_23.webp` | `assets/images/` (new file) |
| `assets/images/lr_img_24.webp` | `assets/images/` (new file) |
| `assets/images/lr_img_29.webp` | `assets/images/` (new file) |
| `assets/images/lr_img_10.jpg` | `assets/images/` (replace the existing one) |
| `assets/videos/lr_video_1.mp4` | `assets/videos/` (replace the existing one) |

## Delete

Nine images are no longer referenced. Delete them in the same commit:

- `assets/images/lr_img_14.jpg`  ← replaced by the `.webp` above
- `assets/images/lr_img_22.jpg`  ← replaced by the `.webp` above
- `assets/images/lr_img_23.jpg`  ← replaced by the `.webp` above
- `assets/images/lr_img_24.jpg`  ← replaced by the `.webp` above
- `assets/images/lr_img_16.jpg`
- `assets/images/lr_img_17.jpg`
- `assets/images/lr_img_18.jpg`
- `assets/images/lr_img_19.jpg`
- `assets/images/lr_img_20.jpg`

## What changed

- **New user flow diagram** (Situation) — the 1x export (4194px).
- **User journeys** — all four maps replaced with the simplified versions:
  1. Registration journey, non-policyholder
  2. Registration journey, policyholder
  3. Login first time journey
  4. Login subsequent journey
- **Zoom** — enlarged diagrams now open fitted to the window at every screen size;
  a click or tap switches to full size. Previously this only happened on phones.
- **Journey Prototype** — new screen recording (734x1592, up from 440x952), with a
  matching poster frame.
- **Step 2** — login method sentence rephrased.
- **Step 4** — closing paragraph about email as username / OTP removed.
- **Findings** — "shipped journeys" carousel removed; "completion rates improved
  across the board" sentence removed.
- **Results against target** — Non-Customer now reads Full (6 steps) / Skip (5 steps).

After the commit: 60 asset files referenced, 60 on disk, none unused.
