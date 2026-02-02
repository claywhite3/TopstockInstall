PROJECT MANIFEST: Vusion App Prototype - Build 2.2
Date: January 27, 2026 Current Focus: Deep Dive Diagnostics & Repair Logic

1. The Camera Repair Chain (Complete)
This flow guides the user from detection to resolution with a "smart" partner feel.

page19.html (Camera Status):

UI: Modern "bubble" buttons for "View Image", "Retest", and "Fix This".

Logic: Simulates failure states (Blurry/KO) to prompt action.

Link: "Fix This" opens the diagnostic tool (camerarepair.html).

camerarepair.html (Diagnostic Questionnaire):

UI: Tri-toggle inputs (Yes / I don't know / No) for Damage, Obstruction, and Dirt.

Smart Logic:

Damage: Hard stop. Pops up "Swap Rail" modal linking to page5.html.

Sequential Fix: If the user marks Obstruction AND Dirty as "Yes", the app chains the modals (Clear Obstruction -> then immediately Open Cleaning Modal).

The Bridge: If no physical issues are found, a specific modal recommends a System Reset.

Redirect: Successfully clearing physical issues triggers a "Verifying Fix..." modal (with spinner) before auto-redirecting to page15.html.

camerareset.html (Hardware Reset Guide):

Content: Step-by-step physical guide (Cap/Battery Cycle + Pinhole Reset).

Visuals: Responsive CSS ensures images (battery-cycle.jpg, reset-pinhole.jpg) fit any screen width perfectly.

Completion: "Actions Completed" triggers a "System Reconnecting" modal before auto-redirecting to page15.html.

2. Core Navigation Updates
page15.html (Modular Settings): The central hub. "Swap Rail" icon in header links to page6.html (or page5.html based on your latest update). Retest logic simulates the "Verification" phase after a repair.

page5.html: Designated as the Swap Rail / Input screen.

Required Assets
Ensure these files are in your project folder:

reset-pinhole.jpg (Close-up of the pinhole)

battery-cycle.jpg (Battery/Cap removal)

left_pic.jpg, center_pic.jpg, right_pic.jpg (Camera views)