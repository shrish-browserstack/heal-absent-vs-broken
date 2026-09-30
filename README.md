# heal-absent-vs-broken

Fixture page for the "absent element vs broken locator" self-healing POC (PTAAA-793).

State is driven by query params:

| param | effect |
|---|---|
| `overlay=1` | full-screen bare container `#vw_overlay_modal_container` (case A) |
| `spinner=1` | full-screen bare `#activity_indicator` (case B) |
| `consent=1` | banner with `#accept_all` "ACCEPT ALL" button (case C, distinctive) |
| `btn=v1|v2` | `#btn_primary` → `#btn_primary_v2`, text unchanged (case D, broken locator control) |
| `heavy=1` | 60 divs with 1.4 KB attributes to overflow the embedding chunk (case E) |

Seed: `?overlay=1&spinner=1&consent=1&btn=v1` · Probe: `?btn=v2`
