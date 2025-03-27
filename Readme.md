# YouTube Blocker Chrome Extension

A simple Chrome extension to block access to **all** YouTube sites (including the mobile site and content delivery networks), helping you stay focused and avoid distractions.

**Purpose:**

This extension is designed to completely block access to YouTube, preventing usage of the platform to aid concentration, reduce screen time, or enforce digital well-being habits.

**Technology:**

- Google Chrome Extension
- Manifest V3
- `chrome.declarativeNetRequest` API

## Features

- **Blocks All YouTube Access:** Prevents navigating to and loading content from `youtube.com`, `m.youtube.com` (mobile site), and associated content delivery networks.
- **Efficient:** Uses Chrome's performant `declarativeNetRequest` API to block requests without significantly impacting browser performance.
- **Minimal Permissions:** Requires only the `declarativeNetRequest` permission and host access to the relevant YouTube domains needed for blocking.

## Installation

As this extension is likely not published on the Chrome Web Store, you need to load it manually as an "unpacked extension":

1.  **Download the Code:**

    - **Option A (Git):** Clone this repository to your local machine:

      git clone [https://github.com/oriventi/youtube_blocker_extension.git](https://github.com/oriventi/youtube_blocker_extension.git)

    - **Option B (ZIP):** Download the source code as a ZIP file (via the "Code" button on GitHub -> "Download ZIP") and unzip it to a folder of your choice.

2.  **Open Chrome Extensions Page:**

    - Open Google Chrome.
    - Type `chrome://extensions` into the address bar and press Enter.

3.  **Enable Developer Mode:**

    - Look for the **Developer mode** toggle switch (usually in the top right corner) and ensure it is enabled.

4.  **Load Unpacked Extension:**

    - Click the "**Load unpacked**" button that should now be visible.

5.  **Select Folder:**

    - Navigate to the folder where you cloned the repository or unzipped the files. Select the main extension folder (the one containing the `manifest.json` file).

6.  **Done:**
    - The "YouTube Blocker" extension should now appear in your list of extensions and be active. Its icon (if provided) may appear in your Chrome toolbar. Attempting to access YouTube should now result in a blocked page (e.g., "ERR_BLOCKED_BY_CLIENT").

## How it Works

This extension utilizes Chrome's `chrome.declarativeNetRequest` API to define a blocking rule. This rule instructs Chrome to block network requests directed to primary YouTube domains (`youtube.com`, `m.youtube.com`) and essential content delivery domains (`googlevideo.com`, `ggpht.com`). By blocking various resource types including the main page (`main_frame`), media (`media`), and scripts (`script`), it effectively prevents the YouTube website and embedded videos from loading and functioning.

## Contributing (Optional)

If you have suggestions or improvements, feel free to open an issue or submit a pull request.

## License (Optional)

This project is licensed under the [MIT License](LICENSE). _(Consider adding a `LICENSE` file with the MIT license text if you wish)_
