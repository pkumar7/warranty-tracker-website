# Privacy Policy for Warranty Manager

**Last Updated:** [Current Date]

## Introduction

Warranty Manager ("we", "our", or "the extension") is committed to protecting your privacy. This Privacy Policy explains how we handle your data when you use our Chrome extension.

## Data Collection and Storage

### Local Storage Only
- **All data is stored locally on your device** using:
  - **IndexedDB** (browser database) - for purchase data and user preferences
  - **Chrome Storage Local** - for notification tracking and temporary state
- **No data is transmitted to external servers**
- **No data is collected by us or any third parties**
- **No analytics or tracking is performed**

### What Data We Store Locally

**In IndexedDB (Purchases Store):**
- Product names
- Purchase prices
- Purchase dates
- Store/retailer names
- Warranty periods
- Receipt photos (if uploaded, stored as base64-encoded images)
- Calculated expiration dates
- Snooze dates (if you snooze reminders for specific purchases)
- Product testing status (boolean flag and date when marked as tested)
- Archived status (boolean flag and date when auto-archived for expired warranties older than 30 days)

**In IndexedDB (Preferences Store):**
- User preferences (default warranty period settings)

**In Chrome Storage Local:**
- Notification tracking data (timestamps of when notifications were sent, stored as `notified-{purchaseId}-{threshold}days`)
- Temporary filter state (when clicking notifications, stored as `filterToProductId`)

### How We Use Your Data
- Data is used solely within the extension to:
  - Display your purchases and warranty information
  - Calculate warranty expiration dates
  - Send browser notifications for expiring warranties (with tracking to prevent duplicates)
  - Filter and sort your purchases
  - Remember your preferences (default warranty period)
  - Export your data (at your request)

## Permissions Used

### Notifications Permission
- Used to send alerts when warranties are expiring soon
- Notifications are generated locally based on your stored data
- You can disable notifications in Chrome settings at any time

### Alarms Permission
- Used to schedule daily checks for expiring warranties
- All processing happens locally on your device

### Storage Permission
- Used to store notification tracking data locally (prevents duplicate notifications for the same warranty threshold)
- Used to temporarily store filter state when clicking notifications (to show the relevant purchase)
- All data remains on your device and is never transmitted externally
- Notification tracking data includes timestamps of when notifications were sent (stored as `notified-{purchaseId}-{threshold}days`)

## Data Export and Deletion

- You can export your data at any time using the Export feature (JSON or CSV format)
- Exported data includes all purchase information stored in IndexedDB
- You can delete individual purchases or all data by uninstalling the extension
- **Purchase data and preferences** are stored in your browser's IndexedDB and can be cleared through browser settings
- **Notification tracking data** is stored in Chrome's local storage and is cleared when you uninstall the extension
- All data is automatically removed when you uninstall the extension

## Third-Party Services

- **We do not use any third-party services**
- **We do not integrate with any external APIs**
- **We do not use analytics or tracking tools**

## Children's Privacy

Our extension does not knowingly collect personal information from children. If you are a parent or guardian and believe your child has provided us with personal information, please contact us.

## Changes to This Privacy Policy

We may update this Privacy Policy from time to time. We will notify you of any changes by updating the "Last Updated" date at the top of this policy.

## Contact

If you have questions about this Privacy Policy, please contact us through the Chrome Web Store listing or GitHub repository.

## Your Rights

- You have full control over your data
- You can export your data at any time
- You can delete your data by removing purchases or uninstalling the extension
- All data processing happens locally on your device

---

**Note:** This extension operates entirely offline and does not transmit any data to external servers. Your privacy is our priority.



