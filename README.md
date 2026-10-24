# Awesome-Mobile-Document-Scanning-App

# Top Mobile Document Scanning App Ecosystem

**Curated List of SaaS Products & Open-Source GitHub Projects**  
*Focused on Offline-First Scanning, On-Device OCR & Privacy-Respecting PDF Generation*  
**Last updated: March 2026**

This repository tracks notable **SaaS platforms** and **open-source projects** for **Mobile Document Scanning Apps**. These tools turn phone camera captures into clean, shareable PDFs — detecting page edges, correcting perspective, enhancing shadows, and embedding searchable text — with a spectrum running from polished commercial apps like Adobe Scan and Microsoft Lens to open-source Android scanners that never upload a single byte.

**Examples** include FairScan, MakeACopy, OSS Document Scanner, ScanBridge, and 拾序 (Shixu) (the category leaders).

**Open-source emphasis**: This section is heavily expanded with every major active project for self-hosting, offline processing, and privacy-first mobile scanning — especially relevant as **CamScanner's data-harvesting history** pushed users toward open-source alternatives, and **FairScan** and **MakeACopy** now rival Adobe Scan's premium features while running entirely on-device [citation:1][citation:2].

Contributions welcome! Open a PR to add/update entries. Keep descriptions factual and link to official sites.

## Table of Contents
- [SaaS/Hosted Platforms](#saas-hosted-platforms)
- [Open-Source GitHub Projects](#open-source-github-projects)
- [How to Contribute](#how-to-contribute)
- [Disclaimer](#disclaimer)

## SaaS/Hosted Platforms

- **Adobe Scan** — **The reference commercial mobile scanner.** Automatic edge detection, OCR, and PDF export with Creative Cloud integration. **Free with Adobe account; premium features require subscription**. **Trade-offs**: cloud sync enabled by default queues uploads to Adobe's servers, and many features are gated behind an account [citation:11]. **Best for Adobe subscribers** wanting seamless integration with Acrobat and Creative Cloud, accepting cloud dependency.

- **Microsoft Lens** — **The Office-integrated scanner.** Captures documents, whiteboards, and business cards with on-device OCR for some functions and OneDrive/Office integration. **Free with Microsoft account**. **Best for Microsoft 365 users** wanting scans that flow directly into Word, PowerPoint, or OneDrive [citation:11].

- **CamScanner** — **The widely-installed commercial scanner.** Edge detection, OCR, and PDF export with cloud backup. **Free tier with watermark and ads; paid Pro**. **Trade-offs**: historical data-harvesting controversies have driven privacy-conscious users to open-source alternatives. **Best for users** already invested in its ecosystem, though open-source options now match its core features without the privacy trade-off [citation:1].

- **Genius Scan** — **The all-round commercial scanner.** On-device edge detection, perspective correction, and OCR once upgraded. **Free tier capped at 30 pages/month; ~$5/month or ~$50 one-time unlocks offline OCR**. **Best for users** wanting polished scanning with on-device processing, accepting the free tier's monthly cap [citation:11].

## Open-Source GitHub Projects

- **FairScan** — **The simple, respectful Android scanner.** **GPLv3 licensed, available on F-Droid, Google Play, and GitHub** [citation:2]. **Designed to be simple and respectful**: snap pages, get a clean shareable PDF in seconds with no manual adjustments, no tracking, no ads, and minimal permissions [citation:2]. **Custom segmentation model** (LiteRT) auto-detects document edges; OpenCV handles perspective correction and image enhancement; Tesseract provides offline OCR; PDFBox-Android generates PDFs [citation:2]. **All processing happens locally on-device** — no cloud processing [citation:2]. **Supports Android 8.0+** with a camera [citation:2]. **Experimental intent API** (`org.fairscan.app.action.SCAN_TO_PDF`) lets other apps request a scan and receive the resulting PDF [citation:2]. **The honest caveat**: **not designed for fine-grained manual control** — it deliberately avoids replicating every feature of other scanners in favor of simplicity [citation:2]. **Best for users** wanting the simplest possible privacy-respecting scanner with automatic edge detection and offline OCR.

- **MakeACopy** — **The privacy-first Android scanner with batch scanning and OCR.** **Open-source, F-Droid compliant**, created by German developer Christian Kierdorf [citation:1]. **Compiles OpenCV from source** rather than using precompiled binaries to guarantee no malicious code enters the build chain [citation:1]. **Multi-page scanning** with reordering and management before export, **Inbox Mode** for auto-saving to a predefined folder (ideal for paperless-ngx, Nextcloud, or Syncthing workflows), and **Last Scans** for quick reuse . **Offline OCR** supports English, German, French, Spanish, Portuguese, Dutch, Polish, Czech, Slovak, Hungarian, Romanian, Danish, Norwegian, Swedish, Turkish, Chinese, Russian, Thai, Arabic, Persian, Hindi, and Greek . **ML-assisted corner detection** via an ONNX model for improved edge detection [citation:1]. **Accessibility Mode** provides spoken and haptic feedback with hardware volume keys as shutter . **The honest caveat**: **OCR quality depends on the PaddleOCR/Tesseract flavor** — the published `paddle` flavor on F-Droid differs from the `standard` Tesseract flavor on GitHub Releases . **Best for Android users** wanting batch scanning, broad OCR language support, and Inbox Mode integration with document management pipelines.

- **OSS Document Scanner** — **The Material You Android scanner with fingerprint lock.** **Open-source (Apache-2.0), available on Play Store and F-Droid** [citation:7]. **Fresh Material You look** with **fingerprint lock**, **real OCR to grab text**, edge detection on white paper, brightness tweaks, and **naming rules with WebDAV backup** [citation:6]. **OpenCV and Tesseract** handle detection and OCR [citation:7]. **The honest caveat**: **building from source requires NativeScript, OpenCV, and Tesseract setup** — the repo does not include the large native libraries, and compilation is non-trivial [citation:7]. **Best for Android users** wanting a polished open-source scanner with OCR and WebDAV backup, accepting the Play Store/F-Droid install path rather than building from source.

- **ScanBridge** — **The WebDAV-connected Android scanner.** **Open-source**, hooks directly into **WebDAV or local storage**, with **cropping that handles odd angles** [citation:6]. **Beats stock apps in bad light**, with real exports that bridge to cloud storage without a hitch [citation:6]. **Best for users** already running a WebDAV server (Nextcloud, ownCloud) who want scans to land directly in their existing storage without a proprietary cloud.

- **拾序 (Shixu)** — **The iPhone-native offline scanner.** **MIT licensed, App Store and TestFlight**, with **完全本地处理** (completely local processing), **无账号、无后端** (no account, no backend) [citation:8]. **Continuous multi-page capture** with background processing queue, **Apple Vision document segmentation and rectangle detection**, perspective correction, shadow compensation, **Vision text-line secondary calibration** to further correct body text perspective, and **A4 multi-page PDF or high-res JPEG export** [citation:8]. **Color, grayscale, and black-and-white modes** adjustable per page, with manual corner adjustment when auto-detection falls short [citation:8]. **The honest caveat**: **iPhone-only** — no Android version [citation:8]. **Best for iPhone users** wanting a fully local, open-source scanner with Vision-powered detection and continuous multi-page capture.

- **Open Note Scanner** — **The minimalist Android scanner.** **Open-source, available on F-Droid**, with on-device detection, saves to a folder you pick, and **no account** [citation:11]. **The safest pick when you need "just scan pages to PDF, nothing else"** — it doesn't send a single byte anywhere [citation:11]. **The honest caveat**: **no OCR** and a functional-but-not-beautiful UI [citation:11]. **Best for users** wanting the absolute minimum network risk — open source, no account, no cloud, no ambiguity.

### Additional Strong Open-Source Options

- **DocMatic** — **The iOS/iPadOS privacy-focused scanner.** **Apache 2.0 licensed** (open-source version on GitHub, App Store version may differ), with document scanning, save & share, **biometric lock**, local storage, and Apple Files integration [citation:3]. **The honest caveat**: **redistribution to app stores is prohibited** without permission, and the App Store version includes additional features not in the repo [citation:3]. **Best for iOS developers** wanting a reference implementation for privacy-focused scanning.

## How to Contribute

1. Fork the repo.
2. Add/edit entries in `README.md` (follow existing format).
3. Include: name, link, 1–2 sentence description, and whether it's SaaS or open-source.
4. Submit PR with a short explanation.

Star the repo if you find it useful!

## Disclaimer

- This is a **community-curated** list — not exhaustive and not an endorsement.
- Mobile document scanning apps differ significantly in privacy posture, OCR capability, and platform support. **CamScanner's historical data-harvesting controversies** make privacy a primary selection criterion for many users [citation:1]. **FairScan and MakeACopy process everything on-device** with no cloud dependency, while **Adobe Scan and Microsoft Lens default to cloud uploads** (though Lens performs some OCR on-device) [citation:2][citation:11]. **Open Note Scanner has no OCR** — it is the safest pick only when you need pure PDF capture with zero network calls [citation:11]. **拾序 is iPhone-only**, and **OSS Document Scanner requires a non-trivial build setup** if you want to compile it yourself rather than install from Play Store/F-Droid [citation:7][citation:8]. **The choice often comes down to platform and OCR needs**: Android users have FairScan (simple) or MakeACopy (batch + broad OCR), iPhone users have 拾序, and users needing zero network risk have Open Note Scanner.
- Self-hosted open-source solutions require proper app installation from F-Droid or GitHub Releases, and awareness that building from source may require Android SDK, NativeScript, OpenCV, and Tesseract toolchains.

---

**Made for mobile users, privacy-conscious professionals, and developers choosing document scanning apps that respect their data.**
Let's make mobile document scanning more open, offline-first, and privacy-respecting.
