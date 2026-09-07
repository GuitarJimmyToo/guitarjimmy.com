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

