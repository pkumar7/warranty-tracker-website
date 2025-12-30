# Warranty Manager Chrome Extension

A Chrome extension to track warranties, manage purchases, and never miss a return window. **100% local storage - your data never leaves your device.**

## Features

- ✅ **Quick Add Mode** - Add purchases in seconds with just product name and warranty period
- ✅ **Progressive Disclosure** - Optional fields (price, date, store, receipt) available when needed
- ✅ **Smart Defaults** - Automatically fills today's date and remembers your preferred warranty period
- ✅ **Visual Status Indicators** - Color-coded cards showing active, expiring, and expired warranties
- ✅ **Actionable Stats Bar** - Click stats to filter purchases by status
- ✅ **Filter Pills** - Easy filtering by Action Needed, Expiring, Active, All, or Expired
- ✅ **Proactive Notifications** - Multi-threshold alerts at 30, 14, 7, and 1 days before expiration
- ✅ **Snooze Reminders** - Temporarily hide notifications for specific purchases
- ✅ **Mark as Tested** - Track which products you've already tested
- ✅ **Auto-Archive** - Expired warranties older than 30 days are automatically archived
- ✅ **Receipt Photo Storage** - Upload and store receipt images (up to 5MB per image)
- ✅ **Import/Export** - Import from JSON/CSV or export your data anytime
- ✅ **100% Local Storage** - All data stored locally (IndexedDB + Chrome Storage)
- ✅ **Privacy-First** - No cloud, no backend, no tracking, no external servers

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

### Adding a Purchase

1. Click the extension icon to open the popup
2. Click "+ Add Purchase" to add a new purchase
3. **Quick Mode (Default):**
   - Enter Product Name (required)
   - Select Warranty Period (required, defaults to 365 days)
   - Click "Save Purchase" - that's it!
4. **Add More Details (Optional):**
   - Click "+ Add more details" to show additional fields
   - Purchase Price (optional)
   - Purchase Date (optional, defaults to today)
   - Store/Retailer (optional)
   - Receipt Photo (optional, max 5MB)

### Managing Purchases

- **Filter by Status:** Click filter pills (Action Needed, Expiring, Active, All, Expired) or click stats bar items
- **Search:** Type in the search bar to find purchases by product name or store (appears when you have 30+ purchases)
- **Purchase Cards:** Each card displays all purchase details including product name, price, store, purchase date, warranty period, and expiration date
- **Action Buttons (on each purchase card):**
  - "📄 Receipt" - View receipt photo (if uploaded)
  - "✅ Dismiss Reminder" - Mark as tested and stop notifications (only shown for urgent items)
  - "📋 File Claim" - Get guidance on filing warranty claims (only shown for urgent items)
  - "✏️ Edit" - Edit purchase details
  - "🗑️ Delete" - Remove purchase from your list

### Data Management

- **Export:** Click Settings → "📥 Export Data" → Choose JSON or CSV format
- **Import:** Click Settings → "📤 Import Data" → Select JSON or CSV file
- **Set Defaults:** Click Settings → "⚙️ Set Defaults" → Set default warranty period
- **Test Notifications:** Click Settings → "🔔 Test Notification" to verify alerts work

## Privacy

- **100% Local Storage** - All data stored on your device using IndexedDB and Chrome Storage
- **No External Servers** - No data is transmitted to any external servers
- **No Tracking** - No analytics, tracking, or data collection
- **No Third-Party Services** - No integrations with external APIs or services
- **Complete Control** - Export or delete your data anytime
- **Transparent Permissions** - Only uses notifications, alarms, and storage (all explained in privacy policy)
- See [PRIVACY_POLICY.md](PRIVACY_POLICY.md) for complete details

## Security

- **Input Validation** - All fields validated with length limits and type checking
- **XSS Protection** - All user inputs escaped and sanitized
- **File Size Limits** - Receipt images limited to 5MB
- **Content Security Policy** - Strict CSP enforced in manifest
- **Minimal Permissions** - Only notifications, alarms, and storage (all justified)
- **No External Requests** - Extension operates entirely offline

## Development

The extension uses:
- **Manifest V3** - Latest Chrome extension standard
- **IndexedDB** - For purchase data storage
- **Chrome Storage API** - For notification tracking and preferences
- **Chrome Notifications API** - For warranty expiration alerts
- **Chrome Alarms API** - For scheduled daily checks
- **ES6 Modules** - Modern JavaScript module system
- **Service Worker** - Background processing for notifications

### Project Structure

- `manifest.json` - Extension configuration
- `popup.html/js/css` - Main UI components
- `background.js` - Service worker for notifications
- `db.js` - IndexedDB operations (popup context)
- `db-worker.js` - IndexedDB operations (service worker context)

## Testing

See [TESTING.md](TESTING.md) for testing warranty notifications.

## Chrome Web Store Submission

See [SUBMISSION_GUIDE.md](SUBMISSION_GUIDE.md) for detailed submission instructions.

## License

MIT


