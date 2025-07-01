# Proliferaite Website

Main developer landing site for Proliferaite - Professional Software Development Services.

## Deployment

This website is automatically synced to the public repository [proliferaite/proliferaite-website](https://github.com/proliferaite/proliferaite-website) via GitHub Actions.

### Sync Process

- **Trigger**: Automatic sync on push to `main` branch when files in `website/proliferaite/**` are modified
- **Target Repository**: `proliferaite/proliferaite-website`
- **Workflow**: `.github/workflows/sync-proliferaite-website.yml`

### Development Workflow

1. Make changes to website content in this folder (`website/proliferaite/`)
2. Commit and push to the `main` branch of this private repository
3. GitHub Action automatically syncs content to the public repository
4. Public repository can be connected to hosting platform (GitHub Pages, Netlify, Vercel, etc.)

### Important Notes

- **Never commit directly** to the `proliferaite/proliferaite-website` repository
- All changes should be made in this private repository
- The sync process will overwrite all content in the public repository
- Ensure you have the `PUBLIC_REPO_TOKEN` secret configured in GitHub Actions

## File Structure

Place your website files directly in this folder:
- `index.html` - Main landing page
- `styles.css` - Styling
- `manifest.json` - Web app manifest
- `wrangler.toml` - Cloudflare Pages configuration
- `assets/` - Static assets (CSS, JS, images)
- `*.html` - Additional pages
- Other static website files

## Cloudflare Pages Configuration

The `wrangler.toml` file configures Cloudflare Pages to:
- Use the root directory as the build output (instead of expecting a "public" folder)
- Deploy static files without a build process
- Handle both production and preview environments

## About Proliferaite

Proliferaite develops professional mobile applications and software solutions, including:
- **PitchGrid**: Professional Video Analysis for Sports
- Custom mobile app development
- Software consulting services 