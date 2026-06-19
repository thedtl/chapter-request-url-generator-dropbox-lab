# Dropbox Chapter Request URL Generator Lab

Experimental copy of the DTL chapter request URL generator for the Dropbox-backed
chapter PDF reader.

The live source repo remains:
https://github.com/thedtl/Chapter-Request-URL-Generator

This lab version points at:

- Reader: `https://thedtl.github.io/chapter-pdf-reader-dropbox-lab/web/image-reader.html`
- Worker: `https://dtl-chapter-reader-dropbox-lab.reference-dfe.workers.dev`

It reads Dropbox-backed PDFs through the lab Worker, extracts PDF bookmarks with
PDF.js, asks the lab Worker to sign one image-reader token per chapter, and
outputs LibGuides-ready HTML.
