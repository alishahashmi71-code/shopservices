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
