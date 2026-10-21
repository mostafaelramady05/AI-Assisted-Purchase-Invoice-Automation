# Explore the n8n workflow as a map

[Back to the project](../README.md)

## What is included

- [Vector workflow map](assets/workflow-map.svg): 132 processing nodes and 146 connections from the uploaded workflow export.
- [Self-contained explorer](workflow-viewer.html): zoom, drag, touch pinch, fullscreen, section navigation, and node-name search. The vector image and search index are embedded, so downloading this single HTML file is enough to use it locally.

Download the HTML using GitHub's **Download raw file** control, then open it in a browser. Use **Section** to jump to document checks, purchase invoice posting, simplified-invoice journals, supplier payments, or the upload/status portal. Search a node name and choose a result to jump to its position. **Fit** returns to the overview; **100%** shows readable native node labels.

The map uses custom styling and curves while preserving supplied node coordinates and connection topology. It is not a screenshot of the n8n editor or an editable/runnable workflow. One setup sticky note is omitted. Solid lines represent main connections; dashed lines represent AI model/parser connections.

## Public data boundary

Only display names, node types, positions, and connections are included. A business-specific portal label is generalized. Node IDs, parameters, custom code, prompts, credentials, execution/pinned data, document contents, and the original workflow export are excluded.

## Publish on GitHub Pages

After merging, configure **Settings → Pages → Deploy from a branch → main → /docs**. The explorer will be served at the Pages site's `workflow-viewer.html` path. GitHub's repository view shows HTML source, so it cannot run the explorer inside the README itself.

When the hosted page is verified, change the README preview link to that live explorer URL. Until then the README links to the downloadable file. No Pages deployment is claimed by these files.
