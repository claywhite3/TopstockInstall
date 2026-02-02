PROJECT MANIFEST: Vusion App Prototype - Build 2 Date: January 23, 2026 Current State: Full "Install" and "Monitoring" flows with Yellow Vusion Theme.

FILE STRUCTURE & LOGIC:

1. Main Menu (Entry Point)

index.html: The new Landing Page.

Button 1: "Install TopStock Rail" -> Links to page2.html.

Button 2: "Monitoring" -> Links to page11.html.

Assets: Uses rail.png and monitoring.png.

2. Installation Flow (The "Happy Path")

page2.html: Install Location Check.

Visual: Map card with map-preview.jpg.

Logic: "Yes" -> page3.html. "No" -> Fake GPS Retry Overlay.

page3.html to page9.html: (Unchanged from Build 1). Covers Aisle Select, Scanning, Camera Overlay, Battery, and Success/Fail loops.

3. Monitoring Flow (New)

page11.html: Store Selection.

Feature: Dropdown menu for Store ID.

Logic: "View List" -> page10.html. "Detect Location" -> page12.html.

page12.html: Monitoring Location Check.

Visual: Same map as Page 2 (map-preview.jpg).

Logic: "Yes" -> page10.html.

page10.html: Aisles Dashboard (High Level).

Visual: List of Aisles (A12, A13, etc) with status counters.

Logic: Clicking "A12" card -> page14.html.

Nav: Back button links to page2.html (per instruction).

page14.html: Aisle Detail View (Deep Dive).

Visual: Specific rail statuses for Aisle 12 (A12.1, A12.2, etc).

Nav: Back button returns to page10.html.

REQUIRED ASSETS (Images):

rail.png (Product thumb)

monitoring.png (Gear/Arrow icon)

map-preview.jpg (Google Maps grid with blue dot)

camera-bg.jpg (For Page 5 scanner)

(Plus original asset list: aisle.jpg, battery-insert.jpg, etc.)