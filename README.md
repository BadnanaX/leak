# LEAK

**A small, browser-based look at browser fingerprinting.**

Websites can read more about your browser than you might expect. LEAK brings those browser-accessible signals together, explains what each one means, and lets you compare a digest of selected readings across scans.

It is an educational project, not a test of whether you are anonymous or impossible to track.

**[Open LEAK](https://BadnanaX.github.io/leak/)** · **[Report a bug](../../issues)**


## What it does

- Checks browser-accessible signals across browser identity, language, display, hardware, rendering, and privacy settings.
- Labels results as readable, heuristic/coarse, or unavailable, rather than treating every reading as equally reliable.
- Builds a digest from selected readings so you can compare scans.
- Offers a JSON report and clipboard export.
- Includes an optional public-IP lookup, initiated only when you choose to run it.

LEAK is a **single HTML file**. There is no build step and no JavaScript package installation.

## Run it locally

1. Download `index.html` from this repository.
2. Open it in a current browser.

For local development, you can also serve the folder with any static HTTP server. Some browser APIs behave differently when a page is opened from a `file://` URL, so a local server may give more representative results.

## Privacy, plainly

The scan runs in your browser. The page does not intentionally send scan results to a LEAK server, set cookies, or write browser storage.

A few details matter:

- **Optional IP lookup:** if you choose the lookup, the page contacts [ipwho.is](https://ipwho.is/). That service receives the request and can see your public IP address. Review its privacy policy before using it.
- **Browser and network behavior:** your browser, extensions, hosting provider, and network may process ordinary connection metadata.
- **Browser signals:** values depend on your browser, operating system, extensions, settings, and available APIs. Some readings are estimates or heuristics.
- **Digest:** a digest is a comparison aid, not proof of a unique or permanent identity. It can change between scans and does not represent every tracking technique a website could use.

The optional lookup is separate from the fingerprint scan. You do not need to use it to scan browser signals.

## What LEAK does not do

LEAK does not claim to measure every fingerprinting technique. It does not read passwords, access local files, or request GPS location. The WebRTC check tests whether the API exists; it does not open a WebRTC connection.

A “readable” result means a page may be able to read that signal under the current conditions. It does not, by itself, mean the signal is dangerous or that a site is tracking you.

## Browser compatibility

LEAK relies on browser APIs that are not implemented or exposed consistently. A missing result can mean the browser does not support an API, the API is restricted, or the check failed. Browser-family detection is best-effort and can be affected by user-agent reduction or spoofing.

Results from different browsers and operating systems are not necessarily directly comparable.

## Project structure

leak/
├── .github/
│   └── workflows/
│       └── pages.yml
├── index.html
├── README.md
├── LICENSE
├── CONTRIBUTING.md
├── CODE_OF_CONDUCT.md
├── SECURITY.md
└── .gitignore

 **What's included?**

+ index.html — The complete LEAK website, including the interface, browser-signal checks, digest generation, and optional IP lookup.

+ README.md — Project overview, features, usage instructions, and privacy notes.

+ LICENSE — MIT License.

+ CONTRIBUTING.md — Guidelines for contributing improvements.

+ CODE_OF_CONDUCT.md — Community participation standards.

+ SECURITY.md — Guidance for reporting security and privacy issues.

+ .gitignore — Excludes common temporary and local development files.

+ .github/workflows/pages.yml — GitHub Actions workflow for deploying LEAK to GitHub Pages.

## Contributing

Small, careful improvements are welcome. Please read [CONTRIBUTING.md](CONTRIBUTING.md) before opening a pull request. Changes should preserve the single-file, no-runtime-dependency approach unless there is a strong reason to change it.

Please do not include personal scan reports, public IP addresses, or identifiable browser details in issues or screenshots.

## Security

If you believe you have found a security or privacy issue, please follow [SECURITY.md](SECURITY.md) rather than posting sensitive details in a public issue.

## License

LEAK is distributed under the MIT License. See [LICENSE](LICENSE).

---

Made to make browser fingerprinting a little easier to understand.
