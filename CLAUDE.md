# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a Mintlify-based documentation site for Nordiska Embedded's API and integration guides. The documentation covers card onboarding processes, invoice management, SEPA integration, and API references.

## Development Commands

### Local Development
```bash
# Install Mintlify CLI globally
npm i -g mintlify

# Start local development server (runs on http://localhost:3000)
mintlify dev

# Use custom port
mintlify dev --port 3333

# Update to latest version
npm i -g mintlify@latest
```

### Validation
```bash
# Check for broken links in documentation
mintlify broken-links
```

## Architecture

### Documentation Structure
- **API Reference**: OpenAPI specification integration from `https://partner-card.test.public.rockerapi.dev/docs/docs.yaml`
- **Card Integration**: Complete onboarding flows for individuals and sole traders
- **Invoice & SEPA**: Payment processing documentation
- **Guides**: Step-by-step integration instructions

### Key Configuration
- **docs.json**: Main configuration file defining navigation, theming, and OpenAPI integration
- **MDX files**: Documentation content with React component support
- **Images**: Located in `/images/` and `/logo/` directories

### Navigation Structure
The site uses a tabbed navigation structure:
- **Guides Tab**: Getting started, card onboarding, invoice/SEPA integration
- **API Reference Tab**: Introduction, errors, and auto-generated API docs

## Content Guidelines

### File Organization
- Card-related content: `/card/` directory
- API documentation: `/api-reference/` directory  
- Invoice/SEPA: `/invoice/` and `/sepa/` directories
- Shared snippets: `/snippets/` directory

### MDX Features
- Support for React components and Mintlify-specific components
- Code blocks with syntax highlighting
- Accordion groups, frames, and info blocks
- Snippet inclusion from `/snippets/` directory

## Troubleshooting

### Common Issues
- **Port conflicts**: Mintlify auto-detects and uses next available port
- **Sharp module errors**: Update to Node.js v19+ and reinstall Mintlify
- **Unknown errors**: Delete `~/.mintlify` folder and retry

### Prerequisites
- Node.js version 19 or higher
- Global Mintlify CLI installation