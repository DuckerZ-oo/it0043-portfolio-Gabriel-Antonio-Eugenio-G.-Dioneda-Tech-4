# M4 — Breakpoints and QA challenges

## Breakpoint decisions

| Breakpoint | Content-based reason |
|---|---|
| `980px` | The three-part playlist row gets cramped as its copy and track list compete for width, so the track list moves below the two main columns. |
| `720px` | The hero copy and illustration become too narrow side by side, so they stack; the five interest cards also move to a two-column arrangement. |
| `520px` | The brand and three navigation links no longer fit comfortably in the header, and the card copy needs a full row, so navigation collapses behind a menu button and cards stack. |

These are content-driven choices reviewed against 320px, 768px, and 1440px viewport layouts. The screenshots in `M4-screens/` are static viewport previews, not browser DevTools captures.

## AI breakpoint challenge

**Challenge:** “At 980px, why move the playlist track list below the copy? A three-column layout may still fit.”  
**Answer:** At widths just under 980px, the wrapper has less than 940px of usable space. Keeping the record, text, and track list side by side narrows the track labels and makes the text column feel compressed. The two-column layout lets the list use the full row.

**Challenge:** “Could the hero remain side by side down to 520px?”  
**Answer:** At 720px, the page wrapper is about 680px wide. Splitting that space leaves roughly 320px per hero column after the gap, which is too tight for the display heading and the illustration together. Stacking preserves room for both.

**Challenge:** “Why use a menu button below 520px instead of wrapping the links?”  
**Answer:** The brand plus three links consume most of a 520px header before padding and gaps are counted. At 320px they cannot sit together without crowding, so the menu button keeps the header readable and gives the links a full-width row when opened.

## Evidence limitation

This workspace did not include an installed browser executable, so the viewport images are static previews based on the HTML/CSS layout and the defect statuses are source-review checks. They are not claims of DevTools device-mode reproduction. To complete the assignment’s hands-on evidence requirement, open the project in a browser, inspect the three widths in DevTools, and replace these previews with browser screenshots if your instructor requires captured evidence.
