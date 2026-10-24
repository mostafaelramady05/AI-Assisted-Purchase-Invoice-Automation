# Explore the workflow in n8n’s canvas

[Open the live workflow](https://mostafaelramady05.github.io/AI-Assisted-Purchase-Invoice-Automation/workflow-viewer.html) · [Back to the project](../README.md)

The viewer uses the official [`<n8n-demo>` web component](https://n8n-io.github.io/n8n-demo-webcomponent/) rather than a custom graph renderer. It retains the workflow’s node types, positions, and connections, with the native n8n canvas controls. The surrounding page provides light/dark mode and fullscreen.

## Presentation data

The embedded presentation copy contains 132 processing nodes and 146 connections. A setup sticky note is excluded, and a business-specific portal label is generalized.

Only node display names, generated presentation IDs, types, type versions, positions, and connection topology are retained. Private node parameters, custom code, prompts, credentials, webhook identifiers, pinned data, and source metadata are excluded. Switch rules use neutral presentation placeholders to retain their visual output ports; these are not the production conditions.

This page demonstrates the workflow structure. It is not the production workflow or a runnable template.

## Dependencies

The page loads `@n8n_io/n8n-demo-component` version `1.0.20` from jsDelivr. The component renders the sanitized presentation data through n8n’s external preview service. Internet access to both services is required; the page displays a retry message if loading takes too long.

No access to the author’s live n8n instance or Daftra account is required. GitHub Pages continues to serve the same `workflow-viewer.html` URL, so existing portfolio and profile links remain valid.
