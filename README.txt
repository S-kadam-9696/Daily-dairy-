MOMENTS DIARY — REPAIRED BUILD

Files
- moments-diary.html: the single-page diary app

Features in this build
- Create, edit, save, search, filter, sort, favorite, pin, duplicate and delete entries.
- One entry supports up to 15 photos, 15 audio files and 5 videos. Each file is limited to 60 MB.
- Attachments can be previewed and downloaded individually.
- Export an entry as TXT, Markdown, standalone HTML (with media embedded), or print it.
- Export the entire diary as a ZIP containing a manifest, entry HTML/Markdown, and original attachment files.
- ZIP creation is built into the app and does not depend on a third-party CDN.
- Theme toggle, focus mode, keyboard save (Ctrl/Cmd+S), prompt helper and a manual “Paste from ChatGPT” helper.

Storage and privacy
- Entries are stored in this browser's localStorage; media is stored in IndexedDB.
- Data stays on this browser/device and is not automatically synced to ChatGPT or another device.
- Use the same browser and same app origin to access saved data. For reliable persistence, serve this file from a local web server or trusted HTTPS site rather than relying on file:// behavior.
- Export ZIP backups regularly. There is no import/restore function in this build.

ChatGPT integration — important limitation
- “Paste from ChatGPT” is a manual paste helper only. The app does not have direct access to your ChatGPT conversation, attachments, or account.
- Automatic two-way integration requires an authenticated, permissioned connector or a backend/API deployment. No API keys or credentials are included in this ZIP.

Verification notes
- JavaScript syntax check passed.
- The ZIP writer was executed in a local test and the generated archive was opened with Python's ZIP reader; CRC validation passed, including a Unicode filename.
- Full interactive browser verification was blocked in this environment, so save/refresh, media upload/playback, print, and all UI buttons have not been claimed as fully end-to-end verified here.
