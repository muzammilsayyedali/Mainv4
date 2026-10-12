# Quote card font

A Bold TTF font file must be placed at `artifacts/api-server/fonts/QuoteFont-Bold.ttf` (for example Inter Bold or Roboto Bold, renamed to `QuoteFont-Bold.ttf`).

This file is required for quote text to render. The production container has no system fonts, so without it the `!quote` / `/quote` image is drawn with no visible text.

The font is registered at startup in `src/bot/quoteImage.ts` under the family name `QuoteFont`. If the file is missing, a warning is logged and the bot keeps running.
