# creative-compass

Creative Compass

A creative space for exploring interests, ideas, and design challenges.

Creative Compass is a free, self-directed web app for collecting interests, exploring creative and income possibilities, capturing thoughts without pressure to act on them, and learning through small experiments. It emphasizes curiosity and flexibility rather than streaks, deadlines, or productivity quotas.

Features

• My interests: Record activities and topics that spark curiosity; explore recurring patterns and themes.

• Idea library: Browse 30 built-in creative/project/income ideas, filter them, and save favorites; add custom ideas.

• Parking lot: Capture thoughts and possibilities without committing to them.

• Experiments: Track low-pressure tests, progress, and reflections.

• Design Playground: Explore 56 hand-authored graphic-design exercises with 6 possible constraints each (336 combinations), filters by design skill and difficulty, optional time suggestions, saved challenges, practice notes, completion history, and an option to turn a challenge into an experiment.

• Reflections: Guided reflection prompts and an open journal.

• Privacy & backups: Save data locally and export/import JSON backups.

The Design Playground does not call an AI API. Its prompts and variations are generated locally from the built-in content.

How it works

This is a static, client-side website built with HTML, CSS, and JavaScript. There is no build system or server database required to run the current edition.

|File                  |Purpose                                                |
|----------------------|-------------------------------------------------------|
|`index.html`          |Main application, styles, scripts, and built-in content|
|`banner.jpg`          |Creative Compass visual branding                       |
|`icon.svg`            |App/favicon artwork                                    |
|`manifest.webmanifest`|Home Screen / installable web app metadata             |
|`README.txt`          |Original distribution notes                            |
|`README.md`           |This project documentation                             |

Keep index.html, banner.jpg, icon.svg, and manifest.webmanifest in the same top-level directory. Relative asset paths in the app assume this layout.

Open locally

You can open index.html in a browser to preview the app. Browser storage behavior can differ for file:// URLs; using a local HTTP server or the published HTTPS site is more reliable when testing saved data.

No package installation, API keys, or environment variables are needed for the current version.

Publish with GitHub Pages

1. Upload the website files into the repository root (not a ZIP archive or an extra containing folder).
2. Go to Settings → Pages in the repository.
3. Under Build and deployment, choose Deploy from a branch.
4. Select the main branch and /(root), then save.
5. Once deployed, open the URL shown in the Pages settings. A typical project URL is https://<username>.github.io/creative-compass/.

To publish an update, commit the revised files to the same configured branch. GitHub Pages will redeploy. If you add the site to an iPhone Home Screen, first open the published HTTPS address in Safari and use Add to Home Screen.

Personal data, privacy, and backups

Important: Data is saved in each user’s browser, not in GitHub.

• Current storage: browser localStorage, under key creative-compass-shareable-v1.

• Storage is specific to the website origin and browser profile. It does not sync across devices, browsers, or different hosting domains.

• Safari and an iOS Home Screen installation may use separate storage. Use a backup to transfer data if needed.

• People using the same browser profile/device may be able to access locally saved entries.

• There are no user accounts, cloud database, analytics, or third-party scripts in the current edition.

• JSON backups are not encrypted; keep them somewhere private.

• Clearing browser/site data can erase saved entries. Encourage occasional backups, especially before switching devices, browsers, or website addresses.

Backup compatibility

The current export format uses format: "creative-compass-shared-backup" and version: 1. The app’s stored data also uses version: 1.

When importing a backup, existing entries are replaced, not merged. Export current data first. The Design Playground state is normalized when loading older compatible data so backups made before that feature can still be restored.

Do not change the storage key, backup format, or data schema casually. If a change is necessary, add a tested migration or backward-compatible import path and document it here.

Design and development principles

• Keep the experience optional and low-pressure: no mandatory streaks, schedules, or deadlines.

• Preserve the existing watercolor-inspired palette, including soft sage/mint, ivory/cream, gold accents, and readable dark text.

• Prioritize comfortable use on phones as well as desktop browsers.

• Maintain clear contrast, keyboard accessibility, readable type, and understandable controls.

• Preserve existing features and user-generated data during changes.

• Review the actual index.html implementation before modifying behavior; this README describes the intended structure but is not a substitute for the code.

• When adding or changing a feature, update this README alongside the code.

Before releasing a change

1. Export a Creative Compass JSON backup from the current live app.
2. Test the changed feature and confirm existing navigation and core features still work.
3. Verify local saving, reload persistence, JSON export/import, and compatibility with older backups.
4. Check the mobile layout, branding assets, and web app manifest.
5. Deploy to the same URL when possible; changing domains separates browser storage.
6. Update this README with changes that affect features, file structure, data format, setup, or deployment.

Known limitations

This version is intentionally local-first and does not include cloud syncing, accounts, encrypted backups, server-side data storage, or AI-generated challenges. A Home Screen shortcut does not turn it into a native iOS application.
