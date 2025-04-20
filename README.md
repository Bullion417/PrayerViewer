# 🙏 PrayerViewer Setup Guide

Welcome to PrayerViewer — a fully customizable, mobile-friendly prayer request display system built for churches and ministries. This guide walks you through setting up and personalizing your viewer to display submissions collected through a Google Form, stored in a linked Google Sheet, and presented using a responsive HTML file.

---

## 🚀 What You Need

- A **Google Form** and linked **Google Sheet** for prayer submissions
- A hosted copy of `PrayerViewer.html`
- A **Google Apps Script Web App** to expose form data as JSON
- (Optional) Custom background and logo image URLs

---

## ⚙️ Configuration Section (Do Not Skip!)
At the top of the HTML file, you’ll find a section marked:
```html
<!-- 🔧 PRAYER VIEWER CONFIGURATION -->
```
This is the **only section** you need to modify. Below is an overview of each variable:

### 📄 Required Variables
| Variable               | Description                                              |
|------------------------|----------------------------------------------------------|
| `viewerTitle`          | Title shown at the top of the screen                    |
| `backgroundImageUrl`   | Full URL to your background image                       |
| `dataSourceUrl`        | Your Google Apps Script Web App URL                     |
| `logoImageUrl`         | Full URL to your logo image (optional)                  |

### 🔤 Font & Layout Options
| Variable            | Purpose                          | Example           |
|---------------------|----------------------------------|-------------------|
| `titleFontSize`     | Size of the viewer title         | "6vw"             |
| `entryFontSize`     | Size of prayer request entries   | "5vw"             |
| `loopFontSize`      | Size of the loop counter text    | "1vw"             |
| `titleSpacing`      | Space between title and entries  | "14vw"            |

### 🎨 Styling
| Variable              | Description                                |
|-----------------------|--------------------------------------------|
| `textShadowColor`     | Shadow color behind text                  |
| `textBoxBgColor`      | Background of text boxes                  |

### 📱 Mobile Overrides
Modify font sizes, logo size, and loop position for smaller screens:
```javascript
const mobileBreakPoint = "768px"; // max width for mobile styling
```
All mobile variants (font size, spacing, etc.) follow the same structure as desktop.

---

## 📡 Getting the Google Apps Script URL
1. Open your Google Sheet.
2. Go to **Extensions > Apps Script**.
3. Paste in the `doGet()` function and deploy as a Web App:
   - Who has access: **Anyone**
   - Copy the deployment URL and use it for `dataSourceUrl`

---

## 🧠 Authorized Personnel Warning
A light-hearted but helpful reminder is embedded in the HTML:
```html
<!-- 🧠 AUTHORIZED PERSONNEL ONLY BEYOND THIS POINT -->
```
Everything *below* that comment runs the viewer logic. Editing it is optional but not recommended unless you know what you’re doing.

---

## 🖼 Recommended Image Sizes
| Image Type    | Recommended Size     | Notes                            |
|---------------|-----------------------|----------------------------------|
| Background    | 1920x1080 (HD)        | Use JPG or PNG                   |
| Logo          | ~500x500 (square)     | Transparent PNG preferred        |

---

## 🛠 Support & Ideas
Need help? Want to share a use case or suggest an improvement?
Reach out to the original project creator or fork the repo to extend functionality!

Blessings as you lift up needs in prayer ✨

