# LinkToVid

A lightweight, responsive video-link helper built for GitHub Pages and Supabase.

## Current features

- Light, responsive interface for desktop, tablet, and mobile.
- Recognizes YouTube, TikTok, Instagram, Facebook, direct video-file URLs, and other web links.
- YouTube preview through the official embedded player; no extraction or bypass of platform download restrictions.
- Direct video links are identified and opened at their source. Browser saving depends on the source server's CORS and download headers.
- Optional Supabase email authentication and private per-user link history.
- Row Level Security ensures users can only read, insert, and delete their own history.

## Stack

- Static HTML/CSS/JavaScript hosted with GitHub Pages.
- Supabase Auth and Postgres.
- Supabase JavaScript client pinned to 2.119.0.

## Supabase

The app uses a dedicated `public.linktovid_history` table in the existing Cardsnoscam project. Existing application tables are not changed.

The table has RLS enabled and owner-scoped policies for authenticated users. The browser uses only the project's publishable key; never put a Supabase secret or service-role key in this repository.

## Run locally

Open `index.html` with a local static server, or enable GitHub Pages for the repository root.

## Important limitations

LinkToVid does not download YouTube videos as standalone files or bypass DRM, access controls, or platform restrictions. For hosted-platform videos, use the platform's own supported viewing, sharing, and download features. Only save direct files when you own them or have permission.
