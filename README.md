# 🌙 nightTab Setup Guide

<p align="center">
  <strong>Restore a ready-made nightTab new-tab setup in a few minutes.</strong><br>
  Download the backup → install nightTab → import the backup → done.
</p>

<p align="center">
  <a href="https://github.com/zombieFox/nightTab"><img src="https://img.shields.io/badge/nightTab-official-111827?style=for-the-badge" alt="nightTab official"></a>
  <a href="https://chromewebstore.google.com/detail/nighttab/hdpcadigjkbcpnlcpbcohpafiaefanki"><img src="https://img.shields.io/badge/Chrome-supported-2563eb?style=for-the-badge&logo=googlechrome&logoColor=white" alt="Chrome"></a>
  <a href="https://addons.mozilla.org/en-US/firefox/addon/nighttab/"><img src="https://img.shields.io/badge/Firefox-supported-2563eb?style=for-the-badge&logo=firefoxbrowser&logoColor=white" alt="Firefox"></a>
</p>

---

## ⚡ Quick Setup

### 1. Download the backup
<p align="center">
  <a href="https://github.com/oxanuragofficial/nighttab-setup-guide-final2/releases/latest/download/nighttab-backup.json">
    <img src="https://img.shields.io/badge/%E2%AC%87%EF%B8%8F%20DOWNLOAD%20BACKUP-nighttab--backup.json-2563eb?style=for-the-badge" alt="Download nightTab backup">
  </a>
</p>

The button downloads the backup asset from the latest release. Save it as `nighttab-backup.json` and keep it available for the import step.

### 2. Install nightTab

- **[Chrome / Chromium browsers](https://chromewebstore.google.com/detail/nighttab/hdpcadigjkbcpnlcpbcohpafiaefanki)**
- **[Firefox](https://addons.mozilla.org/en-US/firefox/addon/nighttab/)**
- **[Official nightTab releases](https://github.com/zombieFox/nightTab/releases)**

### 3. Restore the setup

Open a new tab → click **⚙️ Settings** → **Data → Restore** → **Import from file** → select `nighttab-backup.json`.

---

## 📦 What is included

The supplied backup is a nightTab export from **version 7.5.0**. It contains the saved configuration and bookmark data for the setup shown in this guide.

The restored page includes groups such as **Cool stuff** and **Dev Sites**, with bookmarks including ChatGPT, PULMS, YouTube, LinkedIn, HackerRank, GeeksforGeeks, LeetCode, GitHub, CodeChef, and Codeforces.

No manual recreation of those bookmarks or theme settings is required; they are part of the imported backup.

---

# 🚀 Step-by-Step Setup

## Step 1 — Download the backup

Click the **DOWNLOAD BACKUP** button in the Quick Setup section.

The file is distributed as a GitHub Release asset:

`nighttab-backup.json`

> The README uses the stable `releases/latest/download/nighttab-backup.json` URL so the link does not need to change when a newer setup release is published.

If the link returns **404**, the repository needs a published release containing an asset named exactly `nighttab-backup.json`. See [Release setup](#-release-and-direct-download) below.

---

## Step 2 — Install nightTab

Install nightTab from the official store or use the required nightTab release.

- [Install from Chrome Web Store](https://chromewebstore.google.com/detail/nighttab/hdpcadigjkbcpnlcpbcohpafiaefanki)
- [Install from Firefox Add-ons](https://addons.mozilla.org/en-US/firefox/addon/nighttab/)
- [View nightTab releases](https://github.com/zombieFox/nightTab/releases)

A browser will show its normal extension-install confirmation.

---

## Step 3 — Open a new tab and locate Settings

Open a new browser tab. The nightTab page should appear.

Use the footer/page controls shown in the screenshot, then click the **⚙️ Settings** button.

<p align="center">
  <img src="docs/images/01-new-tab-settings.png" alt="nightTab new tab with Settings button highlighted" width="760">
</p>

The screenshot is cropped to the relevant nightTab controls only. The highlighted control is the **Settings** button.

---

## Step 4 — Open Data → Restore

In Settings, select **Data**, then select **Restore**.

<p align="center">
  <img src="docs/images/02-data-restore.png" alt="nightTab Data and Restore controls" width="760">
</p>

The highlighted areas show the **Data** section and its **Restore** option.

---

## Step 5 — Import the downloaded backup

On the Restore page, click **Import from file**.

<p align="center">
  <img src="docs/images/03-import-file.png" alt="nightTab Import from file button" width="700">
</p>

Select the file downloaded in Step 1:

```text
nighttab-backup.json
```

Use the supplied backup file without editing its contents.

---

## Step 6 — Verify the restored setup

Return to the new-tab page after the import completes.

The supplied configuration should restore the bookmark groups and appearance represented by the backup.

<p align="center">
  <img src="docs/images/04-result.png" alt="Restored nightTab bookmark setup" width="1000">
</p>

---

## 🔄 Complete Workflow

```text
Download backup
      ↓
Install nightTab
      ↓
Open new tab
      ↓
⚙️ Settings
      ↓
Data → Restore
      ↓
Import from file
      ↓
nighttab-backup.json
      ↓
Restored setup ✓
```

---

# 📥 Release and Direct Download

The repository is configured so the backup can be distributed as a GitHub Release asset with one stable download URL.

### Release asset name

```text
nighttab-backup.json
```

### Stable direct-download URL

```text
https://github.com/oxanuragofficial/nighttab-setup-guide2/releases/latest/download/nighttab-backup.json
```

### Publishing a new setup release

Create and push a version tag:

```bash
git tag v1.0.0
git push origin v1.0.0
```

The included GitHub Actions workflow creates the release and uploads:

```text
backup/nighttab-backup.json
```

as the release asset `nighttab-backup.json`.

After the workflow completes, the **DOWNLOAD BACKUP** button in this README points to that asset automatically.

### Manual release option

If you prefer to create the release manually:

1. Open **[Releases](https://github.com/oxanuragofficial/nighttab-setup-guide2/releases)**.
2. Create a release such as `v1.0.0`.
3. Upload `backup/nighttab-backup.json`.
4. Keep the asset filename exactly `nighttab-backup.json`.
5. Publish the release.
6. Test the direct-download URL above.

Do not use the repository `blob` URL as the README download button.

---

# 📁 Repository Structure

```text
nighttab-setup-guide2/
│
├── README.md
├── LICENSE
├── SECURITY.md
├── CONTRIBUTING.md
├── REPO_PLAN.md
├── .gitignore
│
├── backup/
│   ├── README.md
│   └── nighttab-backup.json
│
├── docs/
│   └── images/
│       ├── 01-new-tab-settings.png
│       ├── 02-data-restore.png
│       ├── 03-import-file.png
│       └── 04-result.png
│
└── .github/
    ├── ISSUE_TEMPLATE/
    │   └── setup-problem.md
    └── workflows/
        └── release.yml
```

---

# 🔐 Backup Safety

A nightTab backup can contain bookmark URLs and other configuration.

Before replacing the supplied backup with a personal export, inspect the JSON and remove private information.

Never publish:

- Passwords
- API keys
- Access tokens
- Authentication credentials
- Private/internal URLs

---

# 🛠 Troubleshooting

### The backup button returns 404

A published release must contain an asset named exactly:

```text
nighttab-backup.json
```

Check **Repository → Releases → latest release → Assets**.

### The backup opens as a GitHub page

Make sure the README button uses:

```text
https://github.com/oxanuragofficial/nighttab-setup-guide2/releases/latest/download/nighttab-backup.json
```

and not a `/blob/main/` repository URL.

### Import from file fails

Confirm that:

1. nightTab is installed and enabled.
2. You opened **Settings → Data → Restore**.
3. You selected `nighttab-backup.json`.
4. The downloaded file is complete and unmodified.

### The interface differs from the screenshots

The exact layout can vary with browser, screen size, zoom, and nightTab version. Follow the visible **Settings**, **Data**, **Restore**, and **Import from file** controls shown in the guide.

---

# 🔗 Official Links

- **[nightTab GitHub](https://github.com/zombieFox/nightTab)**
- **[nightTab Releases](https://github.com/zombieFox/nightTab/releases)**
- **[Chrome Web Store](https://chromewebstore.google.com/detail/nighttab/hdpcadigjkbcpnlcpbcohpafiaefanki)**
- **[Firefox Add-ons](https://addons.mozilla.org/en-US/firefox/addon/nighttab/)**

---

# 🤝 Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md).

---

# 📄 License

This repository contains setup documentation and configuration data for nightTab. It is not the nightTab extension itself.

See [LICENSE](LICENSE).

---

<p align="center">
  <strong>Download. Install. Restore. Done.</strong>
</p>
