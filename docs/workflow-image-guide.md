# Interactive workflow explorer

[Back to the project](../README.md)

## Open in your browser

[Explore the live workflow](https://mostafaelramady05.github.io/AI-Assisted-Purchase-Invoice-Automation/)

The site entry point redirects to `workflow-viewer.html`. Once GitHub Pages is enabled, visitors can open the explorer directly without downloading a file or signing in.

Use **Section** to jump between document checks, purchase invoices, journals, supplier payments, and the portal. Search a node name, select a result, and zoom or drag to inspect it. **Fit** returns to the full graph.

## One-time hosting setup

After merging, a repository administrator must select **Settings → Pages → Source: Deploy from a branch → Branch: main → Folder: /docs → Save**. The page is not live until GitHub completes the deployment. Check the URL above after deployment.

GitHub Markdown does not run the interactive HTML page inside a README. The large link at the top of the README opens the hosted page instead.

## What is shown

132 processing nodes and 146 connections reconstructed from the supplied export, preserving positions and topology with custom presentation styling. One setup note is omitted. Solid lines represent main connections; dashed lines represent model/parser links.

The map includes display labels, types, coordinates, and connections only. It excludes the original export, parameters, code, prompts, credentials, IDs, and execution/pinned data. It is a presentation map, not an editable or executable workflow.

## Offline option

The self-contained [HTML explorer](workflow-viewer.html) can also be downloaded and opened locally.
