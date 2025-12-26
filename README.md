# Warranty Manager Chrome Extension

A Chrome extension to track warranties, manage purchases, and never miss a return window. **100% local storage - your data never leaves your device.**

## Features

- ✅ Add purchases manually with all details
- ✅ View all purchases with sorting and filtering
- ✅ Automatic warranty tracking with visual indicators
- ✅ Browser notifications for expiring warranties
- ✅ Receipt photo storage (up to 5MB per image)
- ✅ Export to JSON/CSV
- ✅ All data stored locally (IndexedDB)
- ✅ Privacy-first: No cloud, no backend, no tracking

## Installation

### From Chrome Web Store (Recommended)
1. Visit the Chrome Web Store listing
2. Click "Add to Chrome"
3. Grant notification permission when prompted

### Developer Installation
1. Clone or download this repository
2. Open Chrome and navigate to `chrome://extensions/`
3. Enable "Developer mode" (toggle in top right)
4. Click "Load unpacked"
5. Select the `warranty-manager` folder
6. The extension icon should appear in your toolbar

## Usage

1. Click the extension icon to open the popup
2. Click "+ Add Purchase" to add a new purchase
3. Fill in all required fields:
   - Product Name (max 200 characters)
   - Purchase Price (0 to 999,999,999)
   - Purchase Date (cannot be in the future)
   - Store/Retailer (max 200 characters)
   - Warranty Period (1 to 36,500 days)
   - Receipt Photo (optional, max 5MB)
4. View all purchases, filter by status, and sort as needed
5. Use "Export" to download your data as JSON or CSV
6. Use "🔔 Test Notifications" to verify notification functionality

## Privacy

- **All data is stored locally** on your device using IndexedDB
- **No data is transmitted** to any external servers
- **No tracking or analytics** are performed
- **Complete control** over your data
- See [PRIVACY_POLICY.md](PRIVACY_POLICY.md) for details

## Security

- Input validation and sanitization
- File size limits for uploads
- XSS protection
- Content Security Policy enforced
- Minimal permissions (only notifications and alarms)

## Development

The extension uses:
- Manifest V3
- IndexedDB for local storage
- Chrome Notifications API
- Chrome Alarms API
- ES6 Modules

## Testing

See [TESTING.md](TESTING.md) for testing warranty notifications.

## Chrome Web Store Submission

See [SUBMISSION_GUIDE.md](SUBMISSION_GUIDE.md) for detailed submission instructions.

## License

MIT


