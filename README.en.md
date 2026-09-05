# Housewarming Guestbook / 新居留言簿

[中文](./README.md) · English

A small real-time guestbook made for a housewarming on January 29, 2026.

Guests can leave a name and a short wish. Messages appear together on the page as hanging cards, open into full notes when clicked, and update through Supabase Realtime.

[Open the guestbook](https://housewarming-beige.vercel.app)

## The page

The interaction stays deliberately small: leave one wish and add it to a shared wall of messages.

The current version includes:

- name and message submission;
- existing messages shown newest first;
- real-time updates through Supabase;
- gently swinging hanging-card visuals;
- a modal for reading the full message and timestamp.

## How it is built

The entire project lives in a single `index.html` file and has no build step.

- **Tailwind CSS CDN** for layout and styling
- **Alpine.js** for form, list, and modal interactions
- **Supabase** for message storage and Realtime updates
- **Google Fonts** for Playfair Display and Noto Serif TC
- **Vercel** for the current deployment

The page reads and writes a `guestbook` table with fields including `name`, `message`, and `created_at`.

## Repository structure

```text
.
├── index.html
└── .gitignore
```

`index.html` contains the page structure, styling, and client-side logic together, preserving the final working shape of this one-off project.

## Current status

This repository is best understood as an archive of a finished digital object. The final feature update introduced the hanging-card presentation and the full-message modal; the project was not expanded into a general-purpose guestbook product afterward.
