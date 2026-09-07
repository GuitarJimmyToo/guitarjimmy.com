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

## 2026-09-07 10:38:00 -07:00

To move your plain HTML/CSS site from Bandzoogle to GitHub Pages using GoDaddy, follow these direct steps.
## 1. Upload your HTML/CSS files to GitHub

* Log into GitHub and create a new public repository.
* Name it exactly yourusername.github.io (replace yourusername with your actual GitHub username).
* Upload your complete site files directly into the repository.
* Ensure your main file is named exactly index.html and sits in the root folder.

## 2. Configure GitHub Pages for your domain

* Inside your new GitHub repository, click Settings at the top.
* Click Pages in the left-hand sidebar menu.
* Scroll down to Custom domain.
* Type guitarjimmy.com into the field and click Save.

## 3. Update your DNS settings in GoDaddy

* Log into your GoDaddy Control Panel.
* Go to your My Products page and click DNS next to guitarjimmy.com.
* Look for an existing CNAME record with the Name www. Edit it so it points to your GitHub URL:
* Type: CNAME
   * Name: www
   * Value: yourusername.github.io (replace with your username)
   * TTL: Default or 1 Hour
* Look for any existing A records pointing to Bandzoogle and delete them.
* Add four new A records to point your root domain to GitHub. Click Add New Record for each one:
* Type: A | Name: @ | Value: 185.199.108.153
   * Type: A | Name: @ | Value: 185.199.109.153
   * Type: A | Name: @ | Value: 185.199.110.153
   * Type: A | Name: @ | Value: 185.199.111.153

## 4. Enable security settings

* Wait anywhere from 5 minutes to a few hours for GoDaddy's DNS changes to update globally.
* Return to the Settings > Pages menu in your GitHub repository.
* Scroll down to Custom domain and check the box for Enforce HTTPS once it becomes available.

If you want, tell me:

* Do you have any audio files or media assets linked in your code?
* Are you using any online contact forms that need to be replaced?

I can share alternatives for features that Bandzoogle used to handle automatically.

## 2026-09-07 10:47:40 -07:00

### Image update

- Added `images/two-horn-accoustic-location-system.jpg` to the See Me gallery.
- Added descriptive alternative text and explicit 640 x 515 intrinsic dimensions.
- Updated the shared photo styling to use `max-width: 100%`, `height: auto`, and `width: auto` so images shrink on narrow viewports without being enlarged past their source resolution.
- Removed lazy loading from the new image so it loads reliably from static hosting.
- Verified the new image loads at 640 x 515, scales down on a 390px viewport, and is not upscaled on desktop.

## 2026-09-07 10:52:07 -07:00

### Homepage feature image

- Moved `images/two-horn-accoustic-location-system.jpg` from the See Me gallery to the homepage hero.
- Added it as a responsive background image with a contained lower placement on phones and a right-side placement on wider screens.
- Capped the background sizing at the image's native 640 x 515 resolution to avoid upscaling and blur.
- Verified the homepage has no horizontal overflow at a 390px viewport and the hero background loads correctly.

## 2026-09-07 13:13:33 -07:00

### Dodger Blue text update

- Added Dodger Blue (`#1e90ff`) as the shared heading color.
- Applied it to the active-site navigation labels, page headings, homepage feature headings, song headings, and visible song-title links.
- Verified the computed browser color is `rgb(30, 144, 255)` and all active pages report no errors.

## 2026-09-07 13:15:37 -07:00

### Welcome copy color update

- Updated the homepage welcome paragraph beginning "Welcome to the home of James Cooper" to Dodger Blue.
- Verified both the homepage heading and welcome paragraph compute to `rgb(30, 144, 255)`.

## 2026-09-07 13:17:42 -07:00

### Highlighted homepage copy

- Styled the homepage heading and welcome paragraph like selected text: white foreground on a Dodger Blue background.
- Applied the background to inline text wrappers so it follows the text instead of filling the entire content block.
- Verified both elements compute to white text on `rgb(30, 144, 255)`.

## 2026-09-07 13:19:03 -07:00

### Transparent homepage copy background

- Changed the homepage highlighted-text background to transparent.
- Kept the foreground text Dodger Blue for readability.
- Verified the computed background is transparent and the foreground is `rgb(30, 144, 255)`.

## 2026-09-07 13:20:28 -07:00

### Semi-transparent homepage copy background

- Changed the homepage copy to white text over a 50%-opacity Dodger Blue background.
- Implemented the background as `rgba(30, 144, 255, 0.5)`.
- Verified both highlighted text elements render with the requested foreground and background colors.

## 2026-09-07 13:21:56 -07:00

### Homepage copy opacity reset

- Reduced the Dodger Blue background opacity from 50% to 25%.
- The background now uses `rgba(30, 144, 255, 0.25)` with white text unchanged.
- Verified the computed browser styles.

## 2026-09-07 13:22:30 -07:00

### Homepage copy opacity increase

- Increased the Dodger Blue background opacity from 25% to 75%.
- The background now uses `rgba(30, 144, 255, 0.75)` with white text unchanged.
- Verified the computed browser styles.

## 2026-09-07 13:23:53 -07:00

### Song title underlines

- Underlined all 10 song title banners in the music section, including `Superman`.
- Used consistent underline thickness and offset for readability.
- Left the `My music` page title ununderlined.

## 2026-09-07 13:47:21 -07:00

### Header wordmark sizing

- Increased the maximum header wordmark size from 5rem to 6rem and widened its limit from 37rem to 42rem.
- Added a mobile-specific limit of 4.75rem and 30rem so the navigation remains compact on phones.
- Verified the logo renders at approximately 343 x 45px on a 390px viewport and 672 x 89px on desktop.

## 2026-09-07 13:50:05 -07:00

### Navigation label sizing

- Increased navigation labels from `.78rem` to `.9rem` on mobile.
- Increased navigation labels to `1rem` on wider screens.
- Verified the labels fit without horizontal overflow at mobile and desktop widths.

