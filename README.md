# Project APEX — Kalkulator Dosis

A browser-based tool to calculate compost/fertilizer dose targets from plot areas.

## Run

Open `index.html` in a modern browser. Manual area entry, pasted area lists, dose/ritase calculations, and CSV export work locally without an API key.

## Automatic map reading

PDF (single page), JPG, and PNG upload with preview are supported. To extract plot areas from a map automatically, enter an Anthropic API key in the settings and select **Baca Peta dengan AI**. The map image is sent to Anthropic for vision processing. Do not publish an API key in a public repository; use a secure backend for a production deployment.

## Calculation

- Target per plot (ton) = area (ha) × target dose (ton/ha)
- Decimal ritase = target per plot (ton) ÷ Baldan capacity (ton/ritase)
- Minimum whole ritase per plot = decimal ritase rounded up

Verify AI-read plot areas against the original map before field application.