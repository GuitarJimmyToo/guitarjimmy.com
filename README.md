# guitarjimmy.com

A responsive, mobile-first personal music site for James Cooper, featuring original recordings, lyrics, photos, and contact information.

## Site Pages

- `index.html` - Homepage and featured hero image
- `about-me.html` - Biography and influences
- `my-music.html` - Recordings, SoundCloud players, and lyrics
- `see-me.html` - Photo gallery
- `contact-me.html` - Email contact page

## Design

- Mobile-first responsive layout
- Semantic HTML landmarks and accessible navigation
- Shared styling in `style.css`
- Responsive typography, images, navigation, and embedded audio
- Dodger Blue heading and navigation accents
- Homepage hero featuring `images/two-horn-accoustic-location-system.jpg`
- Image sizing capped to avoid unnecessary upscaling and blur

## Assets

- `images/` contains logos, photographs, and recording artwork
- `music/` contains downloadable MP3 files
- `development-log/` contains dated project notes
- `_Archive/` contains older site versions and is not part of the active navigation

## Running Locally

This is a static HTML and CSS site with no build step or package installation required.

Open `index.html` directly in a browser, or serve the project directory with any static file server. For example, if Python is installed:

```powershell
python -m http.server 4173
```

Then visit `http://localhost:4173/`.

## Deployment

The site can be deployed to any static hosting provider, including GitHub Pages. Upload the project files while preserving the relative paths to the HTML pages, `style.css`, `images/`, and `music/`.

## Editing Notes

- Use forward slashes in asset URLs, including paths containing spaces.
- Keep image `width` and `height` attributes when adding fixed-format images to preserve layout stability.
- Test narrow phone widths after changing navigation or hero content.
- The music page uses externally hosted SoundCloud embeds, so those players require an internet connection.
