# Pose Library

288 poses and 1,439 gray 3D mannequin reference images, in 4 series and 5 camera angles. Open `index.html` in a browser. The pictures are in the `images/` folder of this repository.

`full_sexy_P018` (Wide Knee Squat) has no low angle. Its low-angle control stays disabled, and the card and details say the low view is missing. The page shows another real angle instead of inventing a picture.

The published site is [https://kigo-hoho.github.io/pose-library/](https://kigo-hoho.github.io/pose-library/).

## Open it on your computer

1. On the repository page, choose **Code → Download ZIP**.
2. Extract the **whole folder**. It needs both `index.html` and `images/`.
3. Double-click `index.html`.

The page and pictures use relative paths, so the gallery still works offline. Pose data is embedded in `index.html`, so opening the file does not need to read `poses.json`.

Copying only `index.html` somewhere else will not bring the pictures with it. All 1,439 JPGs sit in the sibling `images/` folder. Without that folder, a card says the image did not load.

## What the page can do

- Filter by series, action category, and camera angle
- Search names, action tags, or IDs
- Save favorites in this browser. If the browser refuses storage, favorites still work until you close the page, then they are forgotten
- Load more poses in batches
- Open a large view, switch angles, copy the current image address, and download that image
- Use the arrow keys for the previous or next pose, and Esc to close
- Work with touch and narrow screens. With “reduce motion” turned on, cards do not tilt

Copy image link copies the address of the page you have open: a `file://` path locally, or the site address when it is hosted. Download uses a normal link to `images/`. If a local page opens the picture instead of saving it, right-click or long-press the image to save it.

## Static hosting

The folder can be published as a static site. Paths are relative, so a subpath such as `/pose-library/` works. `.nojekyll` in the repository root tells GitHub Pages to serve the files as they are.

## Files

| Path | Contents |
| --- | --- |
| `index.html` | Gallery page, with the dataset embedded |
| `images/` | 1,439 JPGs, 126,617,727 bytes in total |
| `poses.json` | Local catalog. Each `url` is `images/filename.jpg`. `sourceUrl` keeps the address used when the file was collected, and the page does not request it |
| `metadata/poses-source.json` | Original metadata, unchanged |
| `metadata/SHA256SUMS` | SHA-256 for every JPG |
| `.nojekyll` | Skip Jekyll when hosting the files as-is |

Image counts by series: Glamour `full_sexy` 399, Full body `full_single` 365, Pairs `pair60` 275, Upper body `upper80v2` 400. Angle counts: front, side, 3/4, and high are 288 each; low is 287.

Check the pictures after extracting the folder:

```bash
sha256sum -c metadata/SHA256SUMS
```

## Rights

These JPGs were collected from the addresses in the original metadata so the gallery can be browsed offline. That metadata does not include a license or a commercial grant. This README does not grant copyright, and it does not say the images may be sold or redistributed. Use them only within the rights you already have in the source material.
