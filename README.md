# Dropbox Chapter Request URL Generator Lab

Experimental copy of the DTL chapter request URL generator for the Dropbox-backed
chapter PDF reader.

The live source repo remains:
https://github.com/thedtl/Chapter-Request-URL-Generator

This lab version points at:

- Reader: `https://thedtl.github.io/reader/web/viewer.html`
- Worker: `https://dtl-chapter-reader-dropbox-lab.reference-dfe.workers.dev`

It reads Dropbox-backed PDFs through the lab Worker, extracts PDF bookmarks with
PDF.js, asks the lab Worker to sign one long-lived chapter token per chapter,
and outputs LibGuides-ready HTML for the protected chapter-only PDF viewer.

Supply an outline containing the selected reader-navigation units, including
selected nested works. A parent's range spans its whole subtree; the next usable
opening outside that subtree is included as the boundary page. Adjacent ranges
therefore overlap and may show neighboring text on a shared page. Start-only
bookmarks do not prove the exact content-end position. Invalid destinations are
skipped, not guessed. Older PDFs mixing scanner bookmarks and generated outlines
are not automatically cleaned, and no wrapper is removed by its title.

Run the focused, PDF-free range checks with `node --test test-chapter-ranges.cjs`.
