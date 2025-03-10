# UpGate Shortcuts Integration Guide

This guide explains how to use the shortcut files provided in this repository to create automations for the UpGate app.

## Files Included

- `app-timer.json`: The JSON representation of the shortcut
- `app-timer.shortcut`: The shortcut file that can be imported into the Shortcuts app
- `app-timer-base64.txt`: The base64-encoded version of the shortcut
- `app-timer-url.txt`: The URL that can be used to import the shortcut directly

## Hosting the Shortcut File on GitHub Pages

To make the shortcut file available for import, you can host it on GitHub Pages:

1. Create a new GitHub repository (e.g., `upgate-shortcuts`)
2. Enable GitHub Pages for the repository
3. Upload the `app-timer.shortcut` file to the repository
4. The shortcut will be available at `https://avartus.github.io/upgate-shortcuts/app-timer.shortcut`

## Direct Import URL

You can use the following URL format to import the shortcut directly:

```
shortcuts://import-shortcut?url=https://avartus.github.io/upgate-shortcuts/app-timer.shortcut
```


## Using the Base64 URL

For iOS 13.1, you can use the base64-encoded URL for direct import. The URL is available in the `app-timer-url.txt` file. You can:

1. Copy the URL from the file
2. Open Safari on your iOS device
3. Paste the URL in the address bar and navigate to it
4. The Shortcuts app will open and prompt you to import the shortcut

## Creating an Automation

After importing the shortcut, you need to create an automation:

1. Open the Shortcuts app
2. Go to the "Automation" tab
3. Tap "+" to create a new automation
4. Choose "App" as the trigger
5. Select the app you want to monitor (e.g., Instagram)
6. Choose "Is Opened"
7. Tap "Next"
8. Tap "Add Action"
9. Search for "Run Shortcut" and select it
10. Choose the imported "App-Timer" shortcut
11. Tap "Next"
12. Turn OFF "Ask Before Running"
13. Tap "Done" to save the automation

## Troubleshooting

If you encounter issues with the shortcut import:

1. **Invalid URL Error**: Make sure the URL is correctly formatted and the shortcut file is accessible
2. **MIME Type Issues**: Ensure the server is serving the shortcut file with the correct MIME type (`application/octet-stream`)
3. **iOS Version Compatibility**: Different iOS versions may have different requirements for shortcut imports

## Technical Details

The shortcut performs the following actions:

1. Waits for a specified time (3 minutes by default)
2. Returns to the Home Screen
3. Opens the UpGate app

The shortcut is designed to be used as part of an automation that triggers when a specific app is opened.
