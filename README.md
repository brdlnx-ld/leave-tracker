# LCY8 Annual Leave Tracker - Setup Guide

## What You Have

- **index.html** — The mobile-friendly web app
- **manifest.json** — Makes it installable as a phone app
- **Code.gs** — Backend code for Google Apps Script (your database)

## Setup Steps (15 minutes)

### Step 1: Create the Backend (Google Apps Script)

1. Go to [https://script.google.com](https://script.google.com)
2. Click **New Project**
3. Delete any code in Code.gs
4. Copy ALL the contents of the `Code.gs` file and paste it in
5. Click **Deploy** > **New Deployment**
6. Click the gear icon next to "Select type" > choose **Web app**
7. Set:- Description: "Leave Tracker API"

- Execute as: **Me**
- Who has access: **Anyone**

1. Click **Deploy**
2. Click **Authorize access** and allow permissions
3. **Copy the Web app URL** — it looks like: `https://script.google.com/macros/s/ABCDEF.../exec`

### Step 2: Connect the Frontend

1. Open `index.html` in a text editor (Notepad works)
2. Find the line that says:``` var API_URL = "YOUR_GOOGLE_APPS_SCRIPT_URL_HERE";

```
3. Replace `YOUR_GOOGLE_APPS_SCRIPT_URL_HERE` with the URL you copied
4. Save the file

### Step 3: Push to GitHub Pages

1. Go to your GitHub account
2. Create a new repository called `leave-tracker` (or whatever you like)
3. Upload all three files (index.html, manifest.json, Code.gs is for reference only)
4. Go to **Settings** > **Pages**
5. Under "Source", select **main** branch and click Save
6. Wait 1-2 minutes — your site will be live at: `https://yourusername.github.io/leave-tracker/`

### Step 4: Share with Your Team

Share the GitHub Pages URL with your team. They can:

- Open it in their phone browser
- Tap the share icon > **Add to Home Screen** (makes it look like a real app)
- Or scan a QR code you create (google "QR code generator" and paste your URL)

## How It Works

- **Team members** open the link > pick their name > tick leave days > submit
- **You** open the same link > tap Dashboard > see everyone's leave
- **Data** is stored in a Google Sheet that gets auto-created in your Google Drive
- **No login required** — works on any phone with internet

## Notes

- The Google Sheet is auto-created the first time the script runs
- Find it in your Google Drive as "LCY8 Leave Tracker Data"
- You can view/edit the raw data directly in that sheet if needed
- Works on any device — phones, tablets, laptops
- No Amazon network or VPN required

```

