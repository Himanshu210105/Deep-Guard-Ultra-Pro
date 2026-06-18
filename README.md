============================================================
  DeepGuard Pro — Complete Setup Guide
============================================================

NEW FEATURES IN THIS VERSION:
  1. EMAIL NOTIFICATIONS
     - User gets email when report is submitted
     - User gets email when admin actions/deletes their report
     - Admin gets email when any new report comes in
    - Admin email: nishantjaat9712@gmail.com

  2. ADMIN DELETE IMAGE
     - Admin can permanently delete any deepfake image
     - User automatically gets email saying image was deleted
     - Deleted images tracked in database

  3. ADMIN INDEPENDENT DETECTION
     - Admin can upload any image/video directly
     - No need to wait for user reports
     - Available at /admin/detect

  4. VIDEO DETECTION (from previous version)
  5. DIGITAL EVIDENCE CERTIFICATE PDF (from previous version)
  6. LOGIN/SIGNUP WITH TWO ROLES (from previous version)

------------------------------------------------------------
STEP 1 — Install libraries
------------------------------------------------------------
  python -m venv venv
  venv\Scripts\activate          (Windows)
  source venv/bin/activate        (Mac/Linux)
  pip install -r requirements.txt

------------------------------------------------------------
STEP 2 — Paste your trained model
------------------------------------------------------------
  model/deepfake_cnn.h5

------------------------------------------------------------
STEP 3 — Run
------------------------------------------------------------
  python app.py
  Open: http://127.0.0.1:5000

------------------------------------------------------------
DEFAULT LOGIN
------------------------------------------------------------
  Admin:  admin / admin123
  User:   user1 / user123

------------------------------------------------------------
EMAIL FLOW
------------------------------------------------------------
  User reports deepfake
    → User gets: "Report Received" email
    → Admin gets: "New Report" alert email

  Admin clicks Save (Actioned/Reviewed)
    → User gets: "Report Actioned" email

  Admin clicks Delete
    → User gets: "Image Deleted" email

------------------------------------------------------------
PAGES
------------------------------------------------------------
  /              Home
  /detect        Upload image or video
  /result/N      Result + certificate download
  /report/N      File complaint
  /history       Scan history
  /admin         Admin panel
  /admin/detect  Admin independent detection
  /verify/ID     Verify certificate by QR code
============================================================
