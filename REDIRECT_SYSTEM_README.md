# PDF Link Tracking System

This system allows you to track when clients click on links from your PDFs, capturing document name, page number, and timestamp information using GoatCounter analytics.

## How It Works

The system uses a dynamic redirect page (`/redirect/`) that:
1. Captures tracking parameters from the URL
2. Sends tracking data to GoatCounter
3. Redirects users to their intended destination
4. Provides a fallback manual link if automatic redirect fails

## Setup Instructions

### 1. Configure GoatCounter

Replace `YOUR_GOATCOUNTER_CODE` in `_layouts/redirect.html` with your actual GoatCounter site code:

```html
<script data-goatcounter="https://YOUR_GOATCOUNTER_CODE.goatcounter.com/count" async src="//gc.zgo.at/count.js"></script>
```

### 2. Build Your Site

```bash
bundle exec jekyll build
bundle exec jekyll serve
```

## Usage Examples

### Basic Redirect

```
https://yourdomain.com/redirect/?url=https://yourdomain.com/contacto
```

### Full Tracking

```
https://yourdomain.com/redirect/?url=https://yourdomain.com/contacto&doc=propuesta-comercial&page=5&ts=2025-01-27T10:30:00Z
```

### WhatsApp Contact

```
https://yourdomain.com/redirect/?url=whatsapp://send?phone=+1234567890&text=Hola&doc=propuesta-comercial&page=3
```

### Email Contact

```
https://yourdomain.com/redirect/?url=mailto:contact@yourdomain.com?subject=Consulta&doc=propuesta-comercial&page=7
```

## URL Parameters

| Parameter | Description | Example |
|-----------|-------------|---------|
| `url` or `redirect` | **Required** - Target URL to redirect to | `https://yourdomain.com/contacto` |
| `doc` or `document` | Document name for tracking | `propuesta-comercial` |
| `page` or `p` | Page number in the document | `5` |
| `ts` or `timestamp` | Timestamp when link was created | `2025-01-27T10:30:00Z` |
| `campaign` or `utm_campaign` | Campaign name for GoatCounter | `pdf-q1-2025` |
| `source` or `utm_source` | Source of the traffic | `pdf` |
| `medium` or `utm_medium` | Medium type | `document` |

## GoatCounter Integration

The system automatically creates GoatCounter events with custom data including:
- Document name
- Page number
- Timestamp
- Campaign information
- Target URL
- Source and medium

This data will appear in your GoatCounter dashboard under Events and Campaigns.

## PDF Link Examples

### For Website Pages
```
https://yourdomain.com/redirect/?url=/contacto&doc=propuesta-comercial&page=5
```

### For WhatsApp
```
https://yourdomain.com/redirect/?url=whatsapp://send?phone=+1234567890&text=Hola,%20me%20interesa%20su%20servicio&doc=propuesta-comercial&page=3
```

### For Email
```
https://yourdomain.com/redirect/?url=mailto:contact@yourdomain.com?subject=Consulta%20sobre%20servicios&body=Hola,%20me%20interesa%20su%20servicio&doc=propuesta-comercial&page=7
```

## Advanced Features

### Custom Campaigns
Create different campaigns for different types of documents:

```
https://yourdomain.com/redirect/?url=/contacto&campaign=propuestas-q1&source=pdf&medium=document
```

### Timestamp Tracking
Include timestamps to track when links were accessed:

```
https://yourdomain.com/redirect/?url=/contacto&ts=2025-01-27T10:30:00Z
```

## Security Considerations

- The redirect page is set to `noindex, nofollow` to prevent search engine indexing
- All parameters are validated before processing
- URLs are sanitized to prevent potential security issues

## Troubleshooting

### Links Not Working
1. Check that the `url` parameter is properly encoded
2. Verify the target URL is accessible
3. Ensure all special characters are URL-encoded

### GoatCounter Not Tracking
1. Verify your GoatCounter code is correct
2. Check browser console for JavaScript errors
3. Ensure the tracking script loads before redirect

### Manual Redirect Required
If automatic redirect fails, users can click the manual link that appears on the page.

## Customization

You can customize the redirect page by modifying:
- `_layouts/redirect.html` - Layout and functionality
- `redirect.md` - Page metadata
- CSS styles in the layout file
- Redirect delay timing (currently 1.5 seconds)

## Support

For issues or questions about this redirect system, please check:
1. GoatCounter documentation: https://www.goatcounter.com/help/
2. Jekyll documentation for custom layouts
3. Browser developer tools for JavaScript errors
