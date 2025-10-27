# GitHub Actions Workflows

## Deploy Documentation

The `deploy-docs.yml` workflow automatically builds and deploys the documentation website to GitHub Pages.

### Setup

To enable GitHub Pages for this repository:

1. Go to repository Settings > Pages
2. Under "Build and deployment", select "Source: GitHub Actions"
3. The workflow will automatically run on pushes to the main branch

### Manual Trigger

You can also manually trigger the workflow from the Actions tab using the "Run workflow" button.

### How it works

1. **Build Job**: Uses the Docker image `ghcr.io/tiogars/mkdocs-docker-image:latest` to build the documentation
2. **Deploy Job**: Uploads the built site to GitHub Pages

The workflow has the necessary permissions configured:
- `contents: read` - to read repository content
- `pages: write` - to deploy to GitHub Pages
- `id-token: write` - for authentication
