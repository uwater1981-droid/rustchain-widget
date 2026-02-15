# RustChain Dashboard Widget

An embeddable dashboard widget for the RustChain network that displays live network statistics.

![Widget Preview](https://via.placeholder.com/400x600/1a1a2e/ffffff?text=RustChain+Dashboard)

## Features

- **Live Data**: Fetches real-time data from RustChain network
- **Dark Theme**: Matches RustChain's aesthetic
- **Mobile Responsive**: Works on all screen sizes
- **Auto-Refresh**: Updates every 60 seconds
- **Zero Dependencies**: Pure HTML/CSS/JS - no frameworks required

## API Endpoints Used

- `/health` - Network health status
- `/epoch` - Current epoch information
- `/api/miners` - Active miners list

## Usage

### Option 1: Embed via iframe

```html
<iframe 
    src="https://your-domain.com/rustchain-dashboard-widget.html" 
    width="400" 
    height="500" 
    frameborder="0">
</iframe>
```

### Option 2: Embed via script tag

```html
<script 
    src="https://your-domain.com/rustchain-dashboard-widget.js"
    data-width="400"
    data-height="500">
</script>
```

### Option 3: Direct usage

Simply open `rustchain-dashboard-widget.html` in a browser.

## Customization

### Colors

Edit the CSS variables at the top of the `<style>` section:

```css
:root {
    --primary-color: #ff6b35;
    --background: linear-gradient(135deg, #1a1a2e 0%, #16213e 50%, #0f3460 100%);
    --text-color: #e8e8e8;
    --accent-color: #4fc3f7;
}
```

### Refresh Rate

Change the refresh interval in the JavaScript:

```javascript
const REFRESH_INTERVAL = 60000; // milliseconds (currently 60 seconds)
```

## API Reference

The widget exposes a global object for external control:

```javascript
// Refresh data manually
window.rustchainDashboard.refresh();

// Get current data
const data = window.rustchainDashboard.getData();
```

## Browser Support

- Chrome 60+
- Firefox 55+
- Safari 11+
- Edge 79+

## Notes

- The widget uses self-signed SSL certificates. Browser security may block requests.
- For production use, consider proxying the API through your own server.

## License

MIT License

## Author

Created by YuntuAtlas_AI for the RustChain bounty program.
