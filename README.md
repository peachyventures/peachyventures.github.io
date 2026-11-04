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

The support page offers Mac Support. The Windows download below is hosted as
an unlisted file. Operator configuration, private signing keys and diagnostic
symbols stay in private infrastructure and build artifacts.

## Unlisted Windows download

The owner approved hosting `files/PeachySupport-windows-x64-2026-11-04.zip`
on 4 November 2026. The archive contains one root entry, `PeachySupport.exe`.
Its accompanying third-party license notices are preserved separately in
`files/PeachySupport-windows-x64-2026-11-04-notices.txt`.
The support HTML and homepage do not link to this Windows download. Anyone
with the URL can retrieve it, and the public source repository also contains it.

The executable is byte-identical to the unsigned x64 CI build from
`peachyventures/PeachyInfra` commit `f92476097f8b083b0fef2e85dd2e0acd8adcfd92`,
run `41681336926`, artifact `13251994900`. Publication repackaged the existing
artifact without compiling or modifying the executable.

- The original CI ZIP SHA-256 is `df9b59bc85df1dbe63d176e77b9c4bf80eefcf8dd2ada7a40badcf80b4f4e03c`.
- The hosted ZIP SHA-256 is `6155ab5067e185c5d2cb0a1d0814f526d05748485180f992073b6712271df724`.
- The executable SHA-256 is `f83079891ba0d46097dbb54e670274fe4e2acae0e09007524ec088e075636846`.

To reproduce this package, verify the original CI ZIP checksum, extract its
`PeachySupport.exe` entry, and zip that executable as the sole root entry.
Preserve the original third-party notices alongside the hosted download.
Recover a bad publication by reverting its website commit and checking the
replacement Pages deployment.
