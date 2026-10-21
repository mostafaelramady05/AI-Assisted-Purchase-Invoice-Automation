# Full workflow image and map-style zoom

[Back to the project](../README.md)

## Available now

[workflow-viewer.html](workflow-viewer.html) is a dependency-free image viewer with cursor-centered zoom, drag/pan, touch pinch, Fit, 100%, and fullscreen controls. Download the HTML file, open it in a browser, and choose a PNG, JPEG, or WebP image. The selected image stays in that browser; the viewer has no upload endpoint.

The full production n8n canvas image has not been supplied, so no full-workflow preview is claimed here.

## Prepare the real image

1. Use a presentation copy of the actual n8n workflow. Keep the real node structure and connections.
2. Review visible labels and open panels for business data, credentials, URLs, and execution values before sharing.
3. Capture at a resolution where node labels are legible at 100%. Enlarging a low-resolution screenshot cannot recover detail. For a large canvas, capture overlapping sections at readable scale and stitch them into one image.
4. Save a reviewed full-resolution PNG as `docs/assets/workflow-full.png`. Keep a smaller preview for the README if needed.
5. Inspect the image at full resolution before publishing it.

## Publish the zoom viewer

After the real image has been added, enable GitHub Pages from the repository's `main` branch and `/docs` folder. The viewer will then be available at the Pages site's `workflow-viewer.html` path. Its default image path is `assets/workflow-full.png`.

GitHub's repository file view displays HTML source; it does not run this viewer inside the README. Use a preview image in the README linked to the published viewer. Do not add the live link until Pages is enabled and verified.

## If the canvas is exceptionally large

A single high-resolution image works for normal workflow screenshots. If it becomes too large to decode or move smoothly on mobile, use a tiled image viewer: divide the image into multiple zoom levels and load only the visible tiles. This viewer currently uses one image and does not claim tiled rendering.
