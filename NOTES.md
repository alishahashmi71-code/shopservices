# Shop Services Page — Change Log

## Round 1 (2026-07-20)

**File:** `modules/module-01-hero-video.html` (Hero with video background)

Brought the module in line with `AppliedLandingPageStyleHandout`:

- **Fonts:** added the explicit `"din-2014", "DIN 2014", "DIN Next", "Helvetica Neue", Helvetica, Arial, sans-serif` stack inline to the eyebrow, h1, both body paragraphs, and both CTA buttons (previously no font-family was declared anywhere in the module).
- **Buttons:**
  - Added the missing `border: 2px solid #007b85` to the primary CTA ("Find a Hose Shop Near You") per the base button rule that every button has a 2px border.
  - Added `line-height: 1.5` to both buttons.
  - Changed `transition` from `all 0.3s ease` to `all 0.25s ease` on both buttons.
  - Corrected hover glow on both buttons from `0 6px 18px rgba(0, 123, 133, 0.40)` to the hero-specific `0 6px 20px rgba(0, 123, 133, 0.50)`.
  - Primary button hover now also updates `border-color` to `#005662` alongside the fill (border must move with the fill per the handout's "hover must change fill, text, AND border together" rule).
  - Normalized button `font-weight` from `bold` keyword to `700` to match the handout's explicit weight ceiling.
  - Left the hero-secondary button's white-fill/teal-text/white-border → teal-fill/white-text/teal-border hover swap as-is; it already matched the handout.
- **Colors:** no changes. Teal `#007b85`/`#005662` and white were already correct, no off-brand or banned colors present.
- Eyebrow ("We Are Applied®") kept white rather than switching to the handout's default teal, since this hero sits over a dark video background — consistent with the handout's own rule that headings on dark sections stay white, and confirmed with the page owner.

No copy, layout, animation, or video/script behavior was changed.

**Re-paste:** module 1 only, into its Custom HTML module in the HubSpot page editor. No HEAD.html or FOOTER.html changes were made in this round.

## Round 2 (2026-07-20)

**File:** `modules/module-02-what-you-get.html` (What You Get from an Applied Hose Shop)

- **Fonts:** added the explicit din-2014 stack to every inline-styled text element (eyebrow, h2, description paragraph, and each of the 7 checklist `<li><span>` items) — none had a font-family declared before.
- **Colors:** the description paragraph used `#444444`, which isn't in the approved gray ramp; corrected to the nearest approved value, `#424242` (gray-800). Eyebrow teal (`#007b85`) and heading/list black (`#000000`) were already correct.
- **Weight:** normalized the h2 from `font-weight: bold` to the explicit `700` for consistency with module 1.
- **Buttons:** none in this module, no changes applicable.
- Left the class-based elements (`aih-overview-badge`, `aih-overview-subhead`, `aih-overview-list`, `aih-overview-image-wrap`, `aih-overview-image-badge`, `aih-overview-image-stat`, `aih-overview-callout`) untouched — their styling lives in HEAD.html, which is outside this round's scope and wasn't provided.

No copy, layout, or animation was changed.

**Re-paste:** module 2 only, into its Custom HTML module in the HubSpot page editor.

## Round 3 (2026-07-20)

**File:** `modules/module-04-spec-to-ship.html` (From Spec to Ship, 4-step process)

- **Fonts:** this module's outermost element (`<section class="aih-process-section">`) was NOT wrapped in `<div class="applied-landing-page">`. Per the handout (section 2b), the shared din-2014 font rule only reaches elements inside that scope wrapper, so this module would have rendered in HubSpot's default theme font regardless of what HEAD.html's CSS says. Added the wrapper div around the module.
- **Colors / buttons:** this module has no inline styles, colors, or buttons at all, everything (`.eyebrow`, `.lead`, `h2`, `h3`, `.aih-process-step-number`, etc.) is class-driven and styled entirely in HEAD.html. I don't have HEAD.html's CSS to inspect, so I can't verify whether those classes currently produce a teal eyebrow, black heading, and din-2014 body text, or need correction. Flagging this rather than assuming — if HEAD.html source is available, send it and I'll audit those rules too.

No copy or layout was changed, only the missing wrapper was added.

**Re-paste:** module 4 only, into its Custom HTML module in the HubSpot page editor.

## Round 4 (2026-07-20)

**File:** `modules/module-05-nahad-certified.html` (NAHAD Certified Fabricators)

- **Fonts:** same missing-wrapper bug as module 4 — the outer `<section>` wasn't inside `<div class="applied-landing-page">`, so the shared din-2014 rule couldn't reach it. Added the wrapper. Also added the explicit din-2014 stack to the CTA button (base button rule: set explicitly, don't rely on inheritance).
- **Colors:** the section background gradient used `#eaeaea`, which isn't in the approved gray ramp; corrected to the nearest approved value, `#eeeeee` (gray-200). `#f5f5f5` was already correct.
- **Buttons ("Talk to an Expert"):**
  - `font-weight: 800` → `700`. This is the exact bug called out in the handout: the Typekit kit has no 800 weight, so an 800 button falls all the way back to Helvetica instead of DIN 2014.
  - Added the missing `border: 2px solid #007b85` (every button needs a border per the base rules).
  - Added `line-height: 1.5`.
  - Changed `transition` from `all 0.3s ease` to `all 0.25s ease`.
  - Hover handler now also sets `border-color` to `#005662` (and mouseout resets it), so the border moves with the fill instead of being left behind.
  - Normalized `background` shorthand to `background-color` to match the other buttons on the page. Glow value (`0 6px 18px @0.40`) was already correct for a non-hero button, no change needed there.
- Left `.aih-nahad-split`, `.aih-nahad-image`, `.aih-nahad-badge`, `.aih-nahad-content`, `.eyebrow`, `h2`, `.body`, `.aih-nahad-list` untouched — class-driven, styled in HEAD.html, not available to audit.

No copy or layout was changed.

**Re-paste:** module 5 only, into its Custom HTML module in the HubSpot page editor.

## Round 5 (2026-07-20)

**File:** `modules/module-03-capabilities-grid.html` (Capabilities Grid, 8 services)

- **Fonts:** same missing-wrapper bug as modules 4 and 5 — the outer `<section class="aih-svc-section">` wasn't inside `<div class="applied-landing-page">`, so the shared din-2014 rule couldn't reach it. Added the wrapper.
- **Colors / buttons:** no inline colors or buttons in this module, no changes applicable. Everything (`.eyebrow`, `.lead`, `h2`/`h3`, `.aih-svc-card`, the `.aih-svc-card--navy` variant, `.aih-svc-card-highlight`) is class-driven and styled in HEAD.html, which isn't available to audit — flagging rather than assuming, same as modules 3 and 4. Worth a specific check once HEAD.html is available: the `--navy` card variant should only use navy as a background/border/accent, never as text color, per the handout.

No copy or layout was changed.

**Re-paste:** module 3 only, into its Custom HTML module in the HubSpot page editor.

## Round 6 (2026-07-20)

**File:** `modules/module-03-capabilities-grid.html` (Capabilities Grid, 8 services)

- Removed the `<div class="aih-svc-card-icon">…</div>` emoji icon from all 8 service cards, per request. No other content, layout, or styling changed.

**Re-paste:** module 3 only, into its Custom HTML module in the HubSpot page editor.

## Round 7 (2026-07-20)

**File:** `modules/module-03-capabilities-grid.html` (Capabilities Grid, 8 services)

- Restored the icon on all 8 cards, per request, but made them less colorful: added an inline `filter: grayscale(70%) opacity(0.85);` to each `.aih-svc-card-icon` div. Emoji glyphs render their own built-in colors and ignore CSS `color`, so a CSS filter is the only way to mute them without swapping in monochrome icon assets (which weren't provided). No other content, layout, or styling changed.

**Re-paste:** module 3 only, into its Custom HTML module in the HubSpot page editor.

## Round 8 (2026-07-20)

**File:** `modules/module-03-capabilities-grid.html` (Capabilities Grid, 8 services)

- Reverted Round 7: removed the `filter: grayscale(70%) opacity(0.85);` from all 8 `.aih-svc-card-icon` divs, per request, so the icons render in their original full color again. No other content, layout, or styling changed.

**Re-paste:** module 3 only, into its Custom HTML module in the HubSpot page editor.
