TopStock Companion — PWA Drop Pack
====================================

WHAT'S INSIDE:
- manifest.json              → PWA manifest (drop in repo root)
- icons/                     → All app icon sizes (drop in repo root)
- *.html                     → All install-flow + entry pages with PWA tags injected

REPO LAYOUT AFTER DROP:
/                            (your repo root, GitHub Pages serves from here)
├── manifest.json
├── icons/
│   ├── icon-72.png
│   ├── icon-96.png
│   ├── ... (all sizes)
│   ├── icon-maskable-192.png
│   ├── icon-maskable-512.png
│   └── favicon.ico
├── index.html               (login — PWA launch target)
├── location.html            (store picker)
├── flow_pick.html           (workflow chooser)
├── install_aisle.html
├── install_section.html
├── install_battery.html
├── install_scan.html
├── install_registering.html
├── install_success.html
├── install_fail.html
└── install_fail_intervention.html

INSTALLING ON A PHONE:
- iOS Safari: Tap Share button → Add to Home Screen
- Android Chrome: Tap menu (⋮) → Install app / Add to Home Screen

WHEN LAUNCHED FROM HOME SCREEN:
- Full screen, no browser chrome
- Status bar tinted #2563EB (your brand blue)
- App name: "TopStock"
- Launches into index.html (login)

NOTES:
- The PWA wrap is opt-in per user (must Add to Home Screen)
- Regular browser visits still work normally
- Updates push the same way (push to GitHub Pages)
- No service worker — app requires network
