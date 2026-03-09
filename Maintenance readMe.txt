# Vusion TopStock - Maintenance Flow

This repository contains the front-end prototypes for the Vusion TopStock Maintenance Flow. The application is designed for field technicians and contractors to locate, diagnose, and resolve hardware issues (Battery, Network, Camera) within assigned store locations.

## 🗂 Application Flow & File Directory

### 1. Entry & Location Selection
The initialization sequence for a technician arriving on-site.
* `index.html`: The main app landing page featuring the entry point to the **Maintenance** flow.
* `maint_location.html`: The store selection interface, allowing users to choose a store via dropdown or GPS detection.
* `maint_detect_gps.html`: The GPS confirmation screen, featuring a simulated loading state and a map preview of the detected location.

### 2. The Maintenance Dashboard
* `assigned_work_landing.html`: The main hub for the selected store. It displays the four primary action categories (**All, Battery, Network, Camera**) with dynamic alert badges and issue counts.

### 3. Issue Map Views
Geospatial representations of pending work, featuring pinch-to-zoom instructions, dynamic active category cards, and map pins that correspond to the exact issue counts.
* `batt_issues_map.html`: Pinpoints 13 battery issues.
* `all_issues_map.html`: Pinpoints all 25 mixed issues.
* `network_issues_map.html`: Pinpoints 4 connectivity issues.
* `camera_issues_map.html`: Pinpoints 8 camera issues.

### 4. Interactive List Views (Checklists)
Detailed checklist views for technicians to execute and clear assigned tasks. Features include simulated network requests ("Checking...", "Ping..."), dynamically updating progress bars, and state transitions (Pending -> Completed).
* `batt_issues_list.html` (13 items): Standard checklist flow for battery replacements.
* `all_issues_list.html` (25 items): Features a condensed progress bar and custom "Multi-Issue" tags with miniature hardware icons (battery/wifi/camera) for overlapping faults.
* `network_issues_list.html` (4 items): Features custom UI tags differentiating between Wi-Fi and Bluetooth connection types, and specific error states (Offline vs. Weak Signal).
* `camera_issues_list.html` (8 items): Features a custom 3-lens array visualizer to explicitly communicate to the technician which specific camera lens in the unit is failing.

## 🚧 Pending / Future Work
* `batt_helpme.html` (and associated help screens): Guided troubleshooting flows are currently paused pending final engineering and hardware designs for the battery replacement procedure.