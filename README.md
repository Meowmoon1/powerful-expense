# 🇸🇬 SG Expense Tracker

A beautiful, offline-first PWA expense tracker designed for daily life in Singapore. Track hawker meals, MRT trips, Grab rides, and more with ease.

![SG Expense Tracker](https://img.shields.io/badge/Made%20for-Singapore-red?style=flat-square)
![PWA Ready](https://img.shields.io/badge/PWA-Ready-blue?style=flat-square)
![Offline First](https://img.shields.io/badge/Offline-First-green?style=flat-square)

## ✨ Features

### Singapore-Specific
- 🍜 **Quick add presets**: Hawker ($5), MRT ($2), Kopi ($1.50), Grab ($15)
- 🏷️ **Local categories**: Hawker, Transport, Kopi/Drinks, Grab/Taxi
- 💵 **SGD currency** formatting throughout
- 📅 **Singapore date format** (DD/MM/YYYY)

### Core Features
- 📊 **Dashboard** with spending summary and budget progress
- 💰 **"Available to Spend"** calculation (like PocketGuard's "In My Pocket")
- 📈 **Monthly budget tracking** with visual progress bars
- 🏷️ **Category-based** expense organization
- 📱 **PWA support** - Install on iPhone/Android home screen
- 🔄 **Offline-first** - Works without internet
- ☁️ **Cloud sync** with Supabase (optional)
- 📤 **CSV export** for records/tax purposes

## 🚀 Quick Start

### Option 1: Local/Offline Only (Simplest)

1. Download the files
2. Open `index.html` in your browser
3. Click "Skip, use offline mode"
4. Start tracking!

Your data is stored in your browser's localStorage.

### Option 2: With Cloud Sync (Recommended)

#### Step 1: Set up Supabase (Free)

1. Go to [supabase.com](https://supabase.com) and create an account
2. Create a new project (remember your database password!)
3. Wait for the project to initialize (~2 minutes)

#### Step 2: Create the Database

1. In your Supabase dashboard, click **SQL Editor** in the sidebar
2. Click **New query**
3. Copy the contents of `supabase-schema.sql` and paste it
4. Click **Run**

#### Step 3: Get Your Credentials

1. Go to **Settings** → **API** in your Supabase dashboard
2. Copy the **Project URL** (looks like `https://xxxx.supabase.co`)
3. Copy the **anon public** key (long string starting with `eyJ...`)

#### Step 4: Connect the App

1. Open the app
2. Paste your Supabase URL and anon key
3. Click "Connect & Start"

Done! Your expenses now sync to the cloud.

## 📱 Install as PWA (iPhone)

1. Open the app in Safari
2. Tap the **Share** button (square with arrow)
3. Scroll down and tap **Add to Home Screen**
4. Tap **Add**

The app will now appear on your home screen like a native app!

## 📱 Install as PWA (Android)

1. Open the app in Chrome
2. Tap the **three dots menu** (⋮)
3. Tap **Add to Home screen** or **Install app**
4. Tap **Add**

## 🗂️ Project Structure

```
sg-expense-tracker/
├── index.html          # Main app (single HTML file with embedded CSS/JS)
├── manifest.json       # PWA manifest for installability
├── sw.js              # Service worker for offline support
├── supabase-schema.sql # Database setup script
├── icons/
│   └── icon.svg       # App icon source
└── README.md          # This file
```

## 🎨 Categories

### Expense Categories
| Icon | Name | Typical Use |
|------|------|-------------|
| 🍜 | Hawker | Hawker centers, kopitiams |
| 🚇 | Transport | MRT, bus fares |
| 🛒 | Groceries | NTUC, Cold Storage, Sheng Siong |
| 🛍️ | Shopping | General shopping |
| 📄 | Bills | SP Services, internet, phone |
| ☕ | Kopi/Drinks | Coffee, bubble tea |
| 🎬 | Entertainment | Movies, activities |
| 💊 | Health | Clinics, pharmacy |
| 🚕 | Grab/Taxi | Ride-hailing, taxis |
| 🍽️ | Dining | Restaurants |
| 📱 | Subscriptions | Netflix, Spotify |
| 📦 | Other | Everything else |

### Income Categories
| Icon | Name |
|------|------|
| 💰 | Salary |
| 💼 | Freelance |
| 🧧 | Angbao |
| 📈 | Investment |
| ✨ | Other |

## 🔒 Privacy & Security

- **Offline mode**: All data stays on your device in localStorage
- **Supabase mode**: Data is encrypted in transit (HTTPS) and at rest
- **No tracking**: We don't track you or sell your data
- **Open source**: You can audit all the code

## 🛠️ Customization

### Change Monthly Budget
1. Go to Settings tab
2. Update the Monthly Budget field
3. Changes save automatically

### Add Custom Quick-Add Buttons
Edit the `QUICK_ADDS` array in `index.html`:

```javascript
const QUICK_ADDS = [
  { icon: '🍜', label: 'Hawker', amount: 5, category_id: 1 },
  { icon: '🚇', label: 'MRT', amount: 2, category_id: 2 },
  // Add your own:
  { icon: '🍔', label: 'McD', amount: 8, category_id: 10 },
];
```

## 📊 Data Export

1. Go to Settings tab
2. Click "Export as CSV"
3. File downloads with all your transactions

CSV format:
```
Date,Description,Category,Amount
2025-01-17,Chicken rice at Maxwell,Hawker,-5.00
2025-01-17,MRT to work,Transport,-2.10
```

## 🤝 Contributing

Contributions welcome! Feel free to:
- Report bugs
- Suggest features
- Submit pull requests

## 📄 License

MIT License - feel free to use for personal or commercial projects.

## 🙏 Acknowledgments

- Built for the Singapore community
- Inspired by Monarch Money, PocketGuard, and YNAB
- Icons from native emoji set

---

Made with ❤️ in Singapore
