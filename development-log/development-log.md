# Development Log

## 2026-09-07 10:17:46 -07:00

### Git setup

- Reviewed Git username and email configuration commands.
- Global configuration:
  - `git config --global user.name "Your Name"`
  - `git config --global user.email "you@example.com"`
- Repository-only configuration can be set by omitting `--global`.
- Configuration can be verified with:
  - `git config --global --get-regexp "user\\.(name|email)"`

### Website redesign

- Replaced the legacy floated layout with a mobile-first responsive design.
- Added responsive navigation for:
  - Home
  - About me
  - My music
  - See me
  - Contact me
- Added modern document structure with semantic HTML landmarks, viewport metadata, page descriptions, accessible navigation, and current-page states.
- Updated the shared stylesheet with:
  - Responsive layout rules
  - Fluid typography
  - Responsive images and embedded media
  - CSS custom properties for colors and sizing
  - Mobile and wider-screen breakpoints
  - Improved focus and hover states
- Preserved the existing music recordings and lyrics.
- Normalized legacy Windows-style asset paths to web-standard forward-slash paths.
- Reworked the About, See Me, and Contact pages for clearer presentation.
- Retained the existing image assets and music files.

### Verification

- No errors were reported for the five HTML pages or the shared stylesheet.
- Tested the homepage at a 390px viewport with no horizontal overflow.
- Tested the music page at a 390px viewport with no horizontal overflow.
- Confirmed that all 16 MP3 links remain available.
- A local Python/Node development server was unavailable, so browser checks used local `file:` URLs.

## 2026-09-07 10:24:05 -07:00

### Music page update

- Replaced the previous music collection with the content from `c:\temp\new_songs.txt`.
- The page now contains exactly these ten songs, in the supplied order:
  1. Superman
  2. In-Between
  3. Always Cage
  4. Factory Farm
  5. Dancing on the Moon
  6. My Bell
  7. Smoking Outside
  8. Gentle the Moon Passes
  9. Freaky Blues
  10. Moving Forward
- Removed the previous song links and lyrical index from the page.
- Verified the page has no reported errors and no horizontal overflow at a 390px viewport.
