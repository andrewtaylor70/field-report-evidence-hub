# Field Report v1.5 - Offline Field Data Collection App 2026

> **Field Report v1.5 is a progressive web app aimed at Android that lets you log site visits without connectivity, keep field evidence organized, and export standalone trip reports.**

[![Platform](https://img.shields.io/badge/Platform-Android%20web%20app-blue?style=flat-square)](https://github.com)
[![Version](https://img.shields.io/badge/Version-v1.5-green?style=flat-square)](https://github.com)
[![Updated](https://img.shields.io/badge/Updated-2026-red?style=flat-square)](https://github.com)
[![License](https://img.shields.io/badge/License-GPL--3.0-yellow?style=flat-square)](LICENSE)
[![Stars](https://img.shields.io/github/stars/andrewtaylor70/field-report-evidence-hub?style=flat-square)](https://github.com/andrewtaylor70/field-report-evidence-hub)

---

<p align="center">
  <a href="https://andrewtaylor70.github.io/field-report-evidence-hub/">
    <img src="https://img.shields.io/badge/Download-Field%20Report%20Latest-brightgreen?style=for-the-badge" alt="Download Field Report">
  </a>
</p>

> **[Direct Download - Field Report v1.5](https://andrewtaylor70.github.io/field-report-evidence-hub/)**

---

[Download Latest Build](https://andrewtaylor70.github.io/field-report-evidence-hub/)

---

## What Field Report Does

When teams need to document inspections and other on-site work with little or no signal, Field Report keeps the workflow moving. As an Android-oriented web app it stays usable offline so you can take photos, enter readings and site conditions, write notes, and mark how each location stands.

Finished trips can be bundled into a ZIP that holds a portable HTML report with photos already inside. Work in progress survives browser restarts through IndexedDB. Season-wide summaries help you scan results across many trips and keep site history current.

---

## What You Can Do

- Log site visits even when the network is down.
- Take pictures with the device camera or the built-in multi-shot camera mode.
- Enter battery voltage, folder scan outcomes, status, faults, and free-form notes.
- Export site records as ZIP archives into the phone Downloads folder.
- Pick up where you left off after a crash or closed tab via IndexedDB local storage.
- Produce trip-level HTML reports that embed the photos you collected.
- Browse season summaries that span more than one trip.
- Export revisioned ZIPs when you amend an existing site record.
- Pin the progressive web app to an Android home screen for quick launch.

---

## Getting It Running

### Use the hosted app

1. Open the current build:

   [Open Field Report](https://andrewtaylor70.github.io/field-report-evidence-hub/)

2. Load the URL in an Android browser.
3. From the browser menu, pick **Add to Home screen** or **Install app**.
4. Start Field Report from the icon that appears on the home screen.

### Serve a local copy

Clone the repo and host the HTML assets with any local web server:

```bash
git clone https://github.com/andrewtaylor70/field-report-evidence-hub.git
cd REPO
```

Open the locally served URL in an Android browser. Serving over HTTP (not bare `file://`) gives more reliable PWA behavior and browser storage.

---

## Day-to-Day Workflow

A common sequence in the field:

1. Start Field Report before you head out.
2. Start a new trip or reopen one you already have.
3. Choose a site and fill in checks, voltages, folder scans, status, faults, and notes as needed.
4. Attach photos with the phone camera or multi-shot camera.
5. Move on to other sites while still offline.
6. Save the trip or site so a ZIP lands in Downloads.
7. Generate the trip HTML report for a shareable package that includes the photos.
8. When you revise a site later, export a revisioned ZIP instead of overwriting history.
9. Open the season summary when you want a cross-trip view.

If the browser or OS stops the session, launch Field Report again on the same device and browser; stored drafts should still be there.

---

## Settings and Storage

There is no separate config file. Everything—sites, trips, measurements, notes, images, and status—is managed inside the UI and held in IndexedDB until you export.

Exports go to the device Downloads folder. Leave enough free space for photos, drafts, ZIP packages, and HTML reports.

---

## Requirements

- Android hardware running a current mobile browser.
- JavaScript with IndexedDB (and related browser storage) enabled.
- Permission to use the camera when capturing photos.
- Local storage space for images and ZIP exports.
- Connectivity only for the first load of the app or when you pull a newer build.
- Offline recording does not need an ongoing network link.
- For local checkouts, prefer an HTTP server over opening files directly.

---

## FAQ

### Does Field Report work fully offline?

Yes for data collection. You can complete site visits without a network and resume drafts from IndexedDB. You only need the network to reach the hosted build the first time or to fetch an update.

### How do I put it on my Android home screen?

Open the hosted build in a compatible Android browser and use **Add to Home screen** or **Install app**. That shortcut opens the PWA.

### Where do exports end up?

Records export as ZIP files under Downloads. Trip reports are self-contained HTML documents with photos embedded.

### What if something interrupts a visit?

Open the app again in the same browser on that device. IndexedDB keeps unfinished records so you can continue.

### Can existing site records be updated?

Yes. Export revisioned ZIP files so newer versions of a site record stay distinct from earlier ones.

### How do photos get into a report?

Capture them while working the site, then build the trip report. The HTML output includes those images inline.

### Camera will not start. What next?

Check that the browser is allowed to use the camera and that you are on a supported Android browser. If access was denied earlier, fix the site permission in browser settings and retry.

### How do I obtain the newest build?

Use the hosted link at the top of this README:

[Download Latest Build](https://andrewtaylor70.github.io/field-report-evidence-hub/)

---

## License

GNU GPL v3.0 - see [LICENSE](LICENSE) for details.
