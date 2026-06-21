# via-browser-custom-logo

This repository contains HTML, CSS, and JavaScript code for creating a custom animated logo in Via Browser. The logo displays a random GIF from Giphy based on a specified tag and includes a loading animation while the GIF is being fetched.

<div align="center">
  <img src="media/example.gif" height="600" alt="example">
</div>

## How to Use

### Prerequisites

- A Giphy API key. You can obtain one by signing up at [Giphy Developers](https://developers.giphy.com/).

### Installation

1. Clone this repository or copy the code.
2. Open the `logo.html` file and replace the placeholders in the `CONFIG` object with your details:

   ```javascript
   const CONFIG = {
     apiKey: '',        // Your Giphy API key
     tag:    'cats',    // Tag to search GIFs by
     rating: 'g',       // Content rating: g, pg, pg-13, or r
   };
   ```

   - `apiKey` — your Giphy API key.
   - `tag` — the search tag for GIFs (e.g., `cats`, `funny`, `nature`).
   - `rating` — content rating filter. Available values:
     - `g` — suitable for all ages (default, safest)
     - `pg` — some mild content
     - `pg-13` — may be inappropriate for children under 13
     - `r` — adult content

3. Open Via Browser and go to **Settings > Customization > Logo**.
4. Select the **HTML Code** option and paste the code from this repository.
5. Save the changes and restart Via Browser if necessary.

## Troubleshooting

- **GIF Not Loading** — ensure that the API key is correct and the specified tag exists on Giphy. If the request fails, a fallback GIF will be displayed automatically.
- **Loading Animation Doesn't Disappear** — check if the API request is successful by opening the browser console and looking for `[GifLoader]` errors.
- **Logo Displays Incorrectly** — make sure the container size (`#gif-container`) meets your requirements.
