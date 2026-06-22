# 📖 AI Leadership Reading Tracker - GitHub Pages Setup

## What You'll Get
✅ A real website URL you can bookmark  
✅ Auto-updates every morning (when your scheduled task runs)  
✅ No popups — just open in your browser  
✅ Completely free (GitHub Pages is free forever)  

---

## Step 1: Create GitHub Account (if you don't have one)
1. Go to https://github.com/signup
2. Sign up with your email
3. Create a username (e.g., `adewunmi-tracker`)
4. Verify your email

---

## Step 2: Create a New Repository
1. Go to https://github.com/new
2. Fill in:
   - **Repository name:** `reading-tracker` (or anything you like)
   - **Description:** AI Leadership Reading Tracker
   - ✅ **Public** (must be public for GitHub Pages to work)
   - ✅ Check "Add a README file"
3. Click **Create repository**

---

## Step 3: Upload Your Files
You have 2 options:

### Option A: Upload via GitHub Website (Easiest)
1. In your new repo, click **Add file** → **Upload files**
2. Download these 3 files from the Cowork outputs folder:
   - `index.html`
   - `data.json`
   - Keep the README that was auto-created
3. Drag & drop the files into the GitHub uploader
4. Click **Commit changes**

### Option B: Upload via Git Command (Advanced)
```bash
git clone https://github.com/YOUR-USERNAME/reading-tracker.git
cd reading-tracker
# Copy index.html and data.json into this folder
git add .
git commit -m "Add tracker files"
git push origin main
```

---

## Step 4: Enable GitHub Pages
1. Go to your repo on GitHub
2. Click **Settings** (top right)
3. Scroll left sidebar → click **Pages**
4. Under "Source", select **Deploy from a branch**
5. Select branch: **main**, folder: **/ (root)**
6. Click **Save**

GitHub will show: _"Your site is published at `https://YOUR-USERNAME.github.io/reading-tracker/`_

---

## Step 5: Bookmark Your Site
Your tracker is now live! 

**Your URL:** `https://YOUR-USERNAME.github.io/reading-tracker/`

Bookmark it. Every morning when your scheduled task runs, the data updates automatically.

---

## Step 6: Connect Your Scheduled Task
Your daily digest task needs to update `data.json` on GitHub.

### What Your Task Should Do:
Every morning at 3:30 PM, after creating the digest:

1. **Capture today's state:**
   - Total articles in tracker
   - How many you read (from localStorage)
   - Completion percentage
   - Action items done

2. **Update data.json:**
   - Add new articles from today's digest
   - Append a snapshot to the `snapshots` array
   - Push to GitHub

### Code to Add to Your Scheduled Task:
```javascript
// After digest runs, update the tracker

const snapshot = {
  date: "2026-06-22",
  total: 4,
  read: 0,
  unread: 4,
  completionPercent: 0,
  mustReadCount: 3,
  actionsDone: 2
};

// Append to data.json snapshots array
// Push changes to GitHub repo
```

---

## Testing It Out

1. Open your tracker URL in a browser
2. Bookmark it ⭐
3. Check off an article (it saves locally)
4. Click **💾 Log Today's Progress**
5. Click **🔄 Refresh Data**
6. Stats update in real-time

---

## FAQ

**Q: Will my bookmarks work forever?**  
A: Yes! GitHub Pages is permanent and free.

**Q: Can I edit the tracker design?**  
A: Yes, edit `index.html` on GitHub and commit changes.

**Q: What if the page doesn't load?**  
A: Make sure both `index.html` and `data.json` are in the root of your repo (same folder level).

**Q: Can I see it on my phone?**  
A: Yes, the URL works on any device.

---

## Next Steps

1. ✅ Create GitHub account (if needed)
2. ✅ Create repo called `reading-tracker`
3. ✅ Upload `index.html` and `data.json`
4. ✅ Enable GitHub Pages
5. ✅ Bookmark your URL
6. ⏳ We'll update your scheduled task to auto-sync data.json

Once you send me your GitHub username, I can help you finalize the auto-update setup.
