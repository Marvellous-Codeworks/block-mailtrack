# Block Mailtrack

A browser extension that blocks email tracking pixels in Gmail — covering Mailtrack and many other spy-pixel services.

A [Marvellous Codeworks](https://marvellouscode.works) project.

> **Origins**: This is a modernised continuation of [gioxx/block-mailtrack](https://github.com/gioxx/block-mailtrack), originally written to block Mailtrack.io tracking in Gmail. That repository has been archived; this is the active home of the project going forward.

---

## What it does

- **Blocks tracking pixels** loaded when you open an email in Gmail, including pixels routed through Gmail's image proxy (`googleusercontent.com`)
- **Hides the Mailtrack signature** injected into composed emails, replacing it with a subtle "Mailtrack pixel blocked" indicator
- Works on **Firefox** (127+) and **Chrome / Chromium**

## Covered services

| Service | Direct block | Gmail proxy block |
|---|---|---|
| Mailtrack | ✓ | ✓ |
| Yesware | ✓ | ✓ |
| HubSpot Sidekick | ✓ | ✓ |
| Bananatag / Staffbase | ✓ | ✓ |
| SalesLoft | ✓ | ✓ |
| Outreach | ✓ | ✓ |
| MixMax | ✓ | ✓ |
| Streak | ✓ | ✓ |
| Apollo.io | ✓ | ✓ |
| Lemlist | ✓ | ✓ |
| GMass | ✓ | ✓ |
| Reply.io | ✓ | ✓ |
| Boomerang | ✓ | ✓ |
| Lavender | ✓ | ✓ |
| Clearbit | ✓ | ✓ |
| Groove | ✓ | ✓ |
| Close.com | ✓ | ✓ |

## Installation

### Firefox
Available on [Firefox Add-ons (AMO)](https://addons.mozilla.org/it/firefox/addon/block-mailtrack/).

To load unpacked for development: `about:debugging` → *This Firefox* → *Load Temporary Add-on* → select `manifest.json`.

### Chrome / Chromium
Go to `chrome://extensions/` → enable *Developer mode* → *Load unpacked* → select the extension folder.

## Known limitations

- Works only in Gmail (mail.google.com)
- Blocking is based on known tracker domains and URL patterns; new or obfuscated trackers may not be caught

## Contributing

Found a tracker that slips through? Open an issue with the domain and a sample proxied URL (you can find these in your browser's Network tab when opening a suspicious email).

## Technical notes

Built with Manifest V3 and `declarativeNetRequest` — no remote server dependencies, all rules are bundled locally in `rules/rules.json`.

## Credits

Original concept: [ksoftlabs/block-mail-track](https://github.com/ksoftlabs/block-mail-track)

## License

See [LICENSE.md](LICENSE.md).
