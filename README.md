# Error Page Templates

This repository contains the error page templates for Deutsche Kraniche Virtual. These templates provide a consistent, branded experience when users encounter errors.

The templates are published to: https://error-templates.dkvirtual.com.

## Quick Start

### Prerequisites
- Hugo (extended version recommended)
- Node.js and npm (for Tailwind CSS)

### Installation

1. **Install Hugo** (if not already installed):
   ```bash
   # macOS
   brew install hugo
   
   # Or download from https://gohugo.io/installation/
   ```

2. **Install dependencies**:
   ```bash
   npm install
   ```

### Development

1. **Serve locally with live reload**:
   ```bash
   hugo serve
   ```
   Visit http://localhost:1313 to preview error pages

2. **Build for production**:
   ```bash
   hugo
   ```
   Static files will be generated in `public/` directory

## Adding New Error Pages

Create a new `.md` file in the `content/` directory:

```yaml
---              # Template layout to use
title: "Error Title"
subtitle: "Brief description of the error"
code: 503
description: "Optional detailed description"
is_cloudflare: true            # Shows Ray ID and Client IP
cf_error_box: "::CLOUDFLARE_ERROR_BOX::"      # Cloudflare error box
cf_error_box_hidden: "::CLOUDFLARE_ERROR_BOX_HIDDEN::" # Hidden CF info
---
```

## Available Parameters

### Required Parameters
- `title` - Main error heading
- `subtitle` - Secondary error message
- `code` - HTTP status code (for reference)

### Optional Parameters
- `description` - Detailed explanation of the error
- `is_cloudflare` - Boolean, shows Cloudflare-specific information (Ray ID, Client IP)
- `cf_error_box` - Cloudflare error box content placeholder
- `cf_error_box_hidden` - Hidden Cloudflare error information placeholder
