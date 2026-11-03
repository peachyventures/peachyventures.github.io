# peachyventures.github.io

## Peachy Support download

GitHub Pages publishes `main` at the repository root to `https://peachy.ventures`.
The unlisted `support.html` download page is available at `/support` and
`/support.html`, with a Mac download button. It is excluded from search indexing
using a robots meta tag and is not linked from the homepage. The page and ZIP
are public, not access-controlled.

The initial Mac download is `files/PeachySupport-macos-2026-11-03.zip`.
Its only top-level item is `Peachy Support.app`; no release notes or separate
text files are included. Required third-party notices remain inside the signed
app bundle. Do not modify bundle contents after signing.

- Build source: `peachyventures/PeachyInfra` commit
  `98ebc8596447dcf6fcde0d21eede5b777ef3afc5`.
- Build run: <https://github.com/peachyventures/PeachyInfra/actions/runs/41684309819>.
- Original artifact: `PeachySupport-macos-universal-19`, ID `13254292592`.
- ZIP SHA-256: `265c08af2f3fd2d898d9b56d5f7df2edaaea490b098a822a6a4f3d66f5f3a688`.
- Universal Apple Silicon/Intel, macOS 11 minimum; Developer ID signed,
  notarized and stapled. Matching diagnostic symbols stay in private build
  artifacts and are not published here.

For an update, copy the verified app-only ZIP to a new versioned filename under
`files/`, update the support page link and this record, then commit/push `main`.
Do not overwrite older archives: versioned URLs keep downloads reproducible.
If repackaging is necessary, use macOS `ditto -c -k --sequesterRsrc --keepParent`
on the signed/stapled `.app`, then verify its extracted signature and ticket.
Confirm the Pages build succeeds and the live ZIP SHA-256 matches the local
file. To recover a bad page/release, revert its website commit and verify the
replacement Pages build; this does not require touching the support gateway.

Only Mac Support is published. Windows Support and the Operator app are not
offered on this page. No model credentials, private signing keys, diagnostic
symbols or Operator configuration belong in this public repository.
