# Uploading to GitHub without deleting the old assets

Placement comes from `index.html`, not from the filenames — every image and
video path in this `index.html` points at a file in this package.

> **Upload `index.html` and the `assets/` folder together, in the same commit.**

If you upload the assets but keep the old `index.html`, the pages will point at
the old numbering and images will land in the wrong slots.

## Naming

| Section | Images | Videos |
| --- | --- | --- |
| Home page | `img_1` | — |
| Case study 1 — Family Banking | `img_2`–`img_18` | `video_1`–`video_4` |
| Case study 2 — Design System | `ds_img_1`–`ds_img_19` | `ds_video_1`, `ds_video_2` |

Case study 2 sits in its own `ds_` namespace, so **none of its 21 files can
collide with anything already in the repo** — they all arrive as new files.

Formats follow the image: `.png` where the artwork needs a transparent
background, `.jpg` everywhere else.

## What happens when the folders merge

GitHub's web uploader merges — it never deletes.

**10 files are overwritten** (same name, new content). This is correct — the new
`index.html` expects the new content at these names:

```
img_1.jpg    img_11.jpg   img_14.jpg   img_15.jpg   img_16.jpg   img_17.jpg
video_1.mp4  video_2.mp4  video_3.mp4  video_4.mp4
```

**33 files are added**, including all of case study 2.

**12 old files are left behind and no longer used.** Dead weight, roughly 9 MB.
Nothing breaks if you keep them; safe to delete from `assets/images/`:

```
img_1.png   img_2.png   img_3.png   img_4.png   img_5.png   img_6.png
img_7.png   img_8.png   img_9.png   img_10.png  img_12.jpg  img_13.jpg
```

Note the extensions — `img_12.jpg` and `img_13.jpg` are the old ones to remove;
the new `img_12.png` and `img_13.png` stay.

## Checking it worked

Open the published page and click into both case studies. If an image is
missing or wrong, it is almost always because `index.html` was not uploaded in
the same commit as the assets.
