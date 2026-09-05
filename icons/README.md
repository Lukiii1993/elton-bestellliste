# Icons — Hinweise

Dieses Verzeichnis enthält das Master‑Icon (`icon.svg`) und kann genutzt werden, um rasch alle benötigten PNG‑Größen zu erzeugen.

Empfohlene PNG‑Größen:
- 16x16 (favicon)
- 32x32 (favicon)
- 180x180 (iOS apple-touch-icon)
- 192x192 (Android/manifest)
- 512x512 (Android/manifest)

Beispiele (ImageMagick / magick):

magick icons/icon.svg -background none -resize 16x16 icons/favicon-16.png
magick icons/icon.svg -background none -resize 32x32 icons/favicon-32.png
magick icons/icon.svg -background none -resize 180x180 icons/apple-touch-180.png
magick icons/icon.svg -background none -resize 192x192 icons/icon-192.png
magick icons/icon.svg -background none -resize 512x512 icons/icon-512.png

PNG‑Optimierung (optional):
- pngquant --ext .png --force icons/*.png
- zopflipng --iterations=500 --filters=01234 --lossy_8bit --lossy_transparent *-512.png optimized-*.png

Nachdem du die PNGs erzeugt, committe sie in `icons/` und aktualisiere ggf. das `manifest.json`.
