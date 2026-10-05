# Consent-Based Selfie Verification Site

This is a GitHub Pages-compatible frontend for a selfie verification flow.

## What it does

1. Visitor opens the link.
2. The browser asks for camera permission.
3. After permission, the front camera opens.
4. The visitor presses "Capture Selfie".
5. The captured selfie is shown for review.
6. The project is ready to connect to a secure backend for storage.

## Important

A browser cannot legitimately turn on a camera or take a photo without the user's camera permission.

## GitHub Pages

Upload `index.html` to a GitHub repository.

Go to:

Repository → Settings → Pages

Select:

- Deploy from a branch
- Branch: main
- Folder: / (root)

Save.

The site must be opened over HTTPS for camera access. GitHub Pages provides HTTPS.

## Connecting storage

The supplied frontend intentionally does not contain a private backend/service-role key.

For production, connect the Upload button to a secure backend or Supabase Storage. Do not put a Supabase service-role key in `index.html`.

A suitable production setup can include:

- private storage bucket
- authenticated/admin access
- unique evidence ID
- server-side timestamp
- upload rate limiting
- file type/size validation
- automatic retention/deletion rules
