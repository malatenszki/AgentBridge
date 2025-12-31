# App Store Submission Checklist

## ✅ Completed (Already Done)

### Code & App
- [x] Privacy descriptions added to Info.plist
  - [x] NSUserNotificationsUsageDescription
  - [x] NSCameraUsageDescription
  - [x] NSLocalNetworkUsageDescription
- [x] App Transport Security configured for local networking
- [x] Welcome/Onboarding screen created
- [x] Notification permission flow fixed (contextual, not on launch)
- [x] Error messages improved (QR expired, etc.)
- [x] Crash prevention (PTYProcess daemon fix)
- [x] No TODO/FIXME/Beta references in code
- [x] Push notification system implemented
- [x] Settings UI with toggle for notifications

### Documentation & Legal
- [x] Privacy Policy created (`docs/privacy.html`)
- [x] Support page created (`docs/support.html`)
- [x] Terms of Service created (`docs/terms.html`)
- [x] Landing page created (`docs/index.html`)
- [x] App Store marketing copy written (`APP_STORE_COPY.md`)

---

## 📋 To Do Before Submission

### 1. App Icon (CRITICAL)
- [ ] Create 1024x1024 PNG app icon
- [ ] Add to `AgentBridge/Assets.xcassets/AppIcon.appiconset/`
- [ ] Verify icon shows in Xcode

**Suggestions:**
- Simple terminal/bridge icon
- Green/cyan color scheme (matches app theme)
- Use SF Symbols or design tool like Figma

### 2. GitHub Pages Deployment
- [ ] Create GitHub repository (if not exists)
- [ ] Push docs folder to repository
- [ ] Enable GitHub Pages in Settings → Pages
- [ ] Select `main` branch and `/docs` folder
- [ ] Verify pages are live

### 3. Update Email Addresses
✅ GitHub URLs already updated to: `malatenszki/AgentBridge`

- [ ] Replace email addresses in HTML files:
  - [ ] `privacy@agentbridge.io` → your email
  - [ ] `support@agentbridge.io` → your email
  - [ ] `legal@agentbridge.io` → your email

**Quick command:**
```bash
cd docs/
# Replace email domain with your actual email
find . -name "*.html" -exec sed -i '' 's/@agentbridge.io/@gmail.com/g' {} +
```

### 4. Screenshots
- [ ] Take 5-7 screenshots on iPhone:
  1. Welcome screen
  2. QR scanner
  3. Session list (with active sessions)
  4. Session detail (terminal output)
  5. Settings page
  6. (Optional) Notification
  7. (Optional) Quick actions
- [ ] Use iPhone 15 Pro Max (6.7") for best quality
- [ ] Add captions using text from `APP_STORE_COPY.md`

**Tips:**
- Use light mode for consistency
- Show real AI agent output (Claude Code is good)
- Make sure no sensitive info is visible

### 5. Build & Test
- [ ] Clean Build Folder (`Cmd + Shift + K`)
- [ ] Build in Release mode
- [ ] Test on real iPhone (not just simulator)
- [ ] Test on physical device:
  - [ ] Welcome screen appears on first launch
  - [ ] QR scanning works
  - [ ] Daemon pairing works
  - [ ] Sessions display correctly
  - [ ] Notifications work
  - [ ] Settings toggle works
  - [ ] No crashes

### 6. App Store Connect Setup

#### App Information
- [ ] App Name: `Agent Bridge`
- [ ] Subtitle: `Monitor AI Agents on iPhone`
- [ ] Primary Category: `Developer Tools`
- [ ] Secondary Category: `Utilities`

#### URLs (Use your GitHub Pages URLs)
- [ ] Privacy Policy URL: `https://malatenszki.github.io/AgentBridge/privacy.html`
- [ ] Support URL: `https://malatenszki.github.io/AgentBridge/support.html`
- [ ] Marketing URL (optional): `https://malatenszki.github.io/AgentBridge/`

#### Description
- [ ] Copy from `APP_STORE_COPY.md` (Version 1 recommended)
- [ ] Keywords: `ai,agent,claude,terminal,remote,monitor,notification,developer,automation,ssh,console`
- [ ] Promotional Text: Copy from `APP_STORE_COPY.md`

#### Screenshots
- [ ] Upload 5-7 screenshots
- [ ] Add captions to each
- [ ] Preview on different device sizes

#### App Review Information
- [ ] Contact Email: Your email
- [ ] Contact Phone: Your phone
- [ ] Demo Account: `Not applicable - QR pairing only`
- [ ] Notes: Copy from `APP_STORE_COPY.md` → "App Review Notes"

**Important:** Include macOS daemon download instructions for reviewers!

### 7. Version & Build Numbers
- [ ] Marketing Version: `1.0`
- [ ] Build Number: `1`

### 8. Pricing & Availability
- [ ] Price: Free
- [ ] Availability: All countries
- [ ] Age Rating: 4+

---

## 🚀 Submission Steps

### Step 1: Archive
1. In Xcode: Product → Archive
2. Wait for archive to complete
3. Window → Organizer should open automatically

### Step 2: Distribute
1. Select your archive
2. Click "Distribute App"
3. Select "App Store Connect"
4. Select "Upload"
5. Choose options:
   - [x] Upload symbols
   - [x] Manage Version and Build Number (automatic)
6. Click "Upload"

### Step 3: App Store Connect
1. Go to [App Store Connect](https://appstoreconnect.apple.com)
2. Select your app
3. Click "+ Version" → Create new version "1.0"
4. Fill in all metadata
5. Add screenshots
6. Add build (may take 10-15 min to process)
7. Complete all sections
8. Submit for Review

---

## ⚠️ Common Rejection Reasons & How We Avoid Them

### ✅ We're Safe Because:

| Rejection Reason | Our Solution |
|-----------------|--------------|
| Missing privacy policy | ✅ Created comprehensive privacy.html |
| Requesting permissions on launch | ✅ Fixed - only when user enables toggle |
| Poor error messages | ✅ Detailed, user-friendly messages |
| Missing functionality explanation | ✅ Welcome screen explains everything |
| Local network without description | ✅ NSLocalNetworkUsageDescription added |
| No support contact | ✅ Multiple contact methods in support.html |
| Placeholder content | ✅ No TODO/Beta/Test references |
| Crashes | ✅ Fixed PTYProcess daemon crash |
| Missing app icon | ⚠️ YOU NEED TO ADD THIS |

---

## 📞 If You Get Rejected

### Don't Panic!
Rejection is normal. Average apps get rejected 1-2 times before approval.

### What to Do:
1. **Read the rejection message carefully**
2. **Fix the specific issue mentioned**
3. **Reply in Resolution Center** explaining your fix
4. **Resubmit**

### Common Quick Fixes:
- Screenshots not clear → Retake with better content
- Metadata unclear → Clarify description
- Missing functionality → Add demo video
- Bug found → Fix and resubmit

---

## ✨ Ready to Submit?

### Final Pre-Flight Check:
```
[ ] App icon added ← MOST IMPORTANT
[ ] GitHub Pages live
[ ] URLs updated in HTML files
[ ] Screenshots ready
[ ] Tested on real device
[ ] All crashes fixed
[ ] Privacy policy accessible
[ ] Support page accessible
[ ] App Store Connect filled out
[ ] Archive created
[ ] Build uploaded
```

### After Submission:
- ⏰ Review time: 24-48 hours typically
- 📧 Watch for emails from Apple
- 🎯 Respond quickly to any questions
- 🎉 Celebrate when approved!

---

## 📚 Resources

- [App Store Review Guidelines](https://developer.apple.com/app-store/review/guidelines/)
- [App Store Connect Help](https://developer.apple.com/help/app-store-connect/)
- [GitHub Pages Docs](https://docs.github.com/en/pages)
- [Human Interface Guidelines](https://developer.apple.com/design/human-interface-guidelines/)

---

## 🎯 Timeline Estimate

- Icon creation: 1-2 hours
- Screenshots: 30 minutes
- GitHub Pages setup: 15 minutes
- App Store Connect form: 30 minutes
- Upload & Submit: 15 minutes

**Total: ~3-4 hours** (excluding review wait time)

Good luck! 🚀
