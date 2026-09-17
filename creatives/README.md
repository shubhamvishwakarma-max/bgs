# Creatives

Static 1080×1080 social creatives built on the backgrounds in this repo.

| File | Background | Output |
| --- | --- | --- |
| `voice-ai-instant-callback.html` | `../bg_01.png` | `voice-ai-instant-callback.png` |
| `lead-qualification-handoff.html` | `../bg_01.png` | `lead-qualification-handoff.png` |
| `lead-qualification-simple.html` | `../bg_01.png` | `lead-qualification-simple.png` |

## Rendering

The HTML is a fixed 1080×1080 stage with locally bundled fonts — Geist for the headline and sub-copy, Geist Mono for the flow visual and CTA (`fonts.css` + `fonts/`),
so it renders identically offline. To re-render after an edit:

```bash
chrome --headless --disable-gpu --no-sandbox --hide-scrollbars \
  --force-device-scale-factor=1 --window-size=1080,1200 \
  --screenshot=out.png --virtual-time-budget=4000 \
  file://$PWD/<creative>.html
# then crop the top 1080×1080 (the extra viewport height avoids clipping the footer bar)
```

The background already carries the headline panel (y 120–355), the corner ticks and the
DoubleTick / Meta footer bar — the composition only adds copy, the flow visual and the CTA.
