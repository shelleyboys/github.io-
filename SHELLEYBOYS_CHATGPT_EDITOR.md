# Shelley Boys ChatGPT Editor Guide

This repository powers the Shelley Boys family and athlete website. Future ChatGPT editing sessions should use this guide before making site updates.

## Repository

- Repository: `shelleyboys/github.io-`
- Default branch: `main`
- Live athlete pages are stored at the repository root.

## Athlete page map

- Demetrus: `demetrus.html`
- Darius: `darius.html`
- Da'Marius: `damarius.html`
- Datavius: `datavius.html`

## Image folder map

All NEW athlete images should go into that athlete's dedicated folder:

- Demetrus: `images/demetrus/`
- Darius: `images/darius/`
- Da'Marius: `images/damarius/`
- Datavius: `images/datavius/`

Do not move or rename older images merely to match this structure. Existing HTML may depend on their current paths.

## Normal update request

The family member editing the site should be able to provide only:

1. Athlete name
2. Sport or activity
3. Season/year or event name
4. Uploaded photos, if any
5. YouTube or YouTube Shorts links, if any
6. Optional notes about what happened

Example request:

`Add these photos to Darius, Basketball Summer 2026, Tournament 3. Add this YouTube link too. He had a strong defensive game.`

ChatGPT should handle the HTML, image paths, YouTube embed conversion, brief copywriting, sidebar updates, and GitHub commit.

## Required workflow for ChatGPT

For every site update:

1. Fetch the CURRENT version of the athlete HTML file from GitHub before editing it.
2. Inspect the existing section structure, sidebar anchors, gallery markup, and video formatting.
3. Preserve all existing content unless the user explicitly asks to remove or replace something.
4. If the requested season/event already exists, add the new material inside that section.
5. If it is a new season/event, create a new `<article>` with a clean unique anchor and add a matching sidebar link.
6. Put new photos in the athlete's dedicated image folder.
7. Use regular full-size images unless the user specifically asks for thumbnails.
8. Convert normal YouTube and Shorts URLs to `https://www.youtube.com/embed/VIDEO_ID` format.
9. Keep video markup responsive and consistent with the page's existing structure.
10. Write short, positive, factual blurbs based only on information the user provides. Do not invent scores, awards, stats, or outcomes.
11. Keep the existing Shelley Boys visual style unless the user specifically requests a redesign.
12. Commit only the requested update and summarize exactly which files changed.

## Image naming convention

For new files, use lowercase names whenever practical and avoid spaces.

Preferred pattern:

`athlete-sport-year-event-##.jpg`

Examples:

- `darius-basketball-2026-tournament3-01.jpg`
- `damarius-football-2026-week2-01.jpg`
- `datavius-flagfootball-2026-week1-01.jpg`
- `demetrus-basketball-2026-ecclesia-01.jpg`

If the uploaded image format is PNG, JPEG, or another normal web image format, preserve the actual extension unless conversion is intentionally performed.

## Safety rules

- Never replace an athlete's entire HTML page from memory.
- Never edit an old cached copy when GitHub can be fetched first.
- Never delete unrelated sections while adding a new section.
- Never change filenames of existing media without also verifying every reference to them.
- Never invent a video ID. Extract it from the supplied link.
- Never overwrite an existing image with a different upload unless the user explicitly asks to replace it.
- If an update touches several files, verify paths before committing.

## Default publishing behavior

For ordinary family content updates, publish directly to `main` after fetching and checking the current files. Use a separate branch or pull request when the user specifically requests an approval/review step or when making a broad redesign.

## What the daughter should have to type

A short natural-language request is enough. She should not need to write HTML.

Good examples:

`These are Datavius flag football photos from Fall 2026 Week 2. Add them to his page and write a short blurb.`

`Put these pictures under Da'Marius Spring 2026 basketball championships and add this video: [YouTube link].`

`Create a new Darius football Fall 2026 section with these photos and this video.`

ChatGPT should ask a follow-up only when a genuinely necessary detail cannot be determined from the uploaded content, current page, or request.
