---
layout: docs
title: FAQ
description: Frequently asked questions.
group: overview
---

Frequently Asked Questions
--------------------------
This page contains answers to some frequently asked questions about ESD.


Authorization Scopes
--------------------
ESD is an add-on for Google Sheets, and as such requires specific authorizations to function. These scopes (ordered by their official google api URLs) are:

- `https://www.googleapis.com/auth/drive`
  - Grants access to Google Drive files and folders.
  - Needed for:
    - File creation when exporting data.
    - Adjusting file contents when exporting data with [Replace existing file(s)](general/replaceexistingfiles.md) enabled.
    - Accessing folders via file picker when setting custom export locations.
- `https://www.googleapis.com/auth/spreadsheets`
  - Grants access to spreadsheet data.
  - Needed to access spreadsheet data when exporting JSON or XML.
- `https://www.googleapis.com/auth/script.container.ui`
  - Grants access to Google's UI.
  - Needed to add ESD UI and menu items.
- `https://www.googleapis.com/auth/userinfo.email`
  - Grants access to email information about the user using ESD.
  - Needed for:
    - Storing and loading settings for ESD.
    - Executing ESD's various processes (when an add-on executes code, it is done under the email of the user)
    
***These scopes are the minimum required scopes needed for ESD to function.*** While it is understandable for some users to be uncomfortable granting ESD access to certain things, every scope used is needed and ESD does not do anything nefarious. Your data is *your* data!
