# ClassRoom Finder — FoCP (CSE-1003)

A responsive classroom information finder prototype for IIIT Bhopal.

## What's included
- `index.html`, `styles.css`, `app.js`: deployable static website.
- `classroom_finder.c`: FoCP companion program demonstrating structures, arrays, functions, loops and switch-case.
- Local browser storage for the prototype's room records and profile settings.

## Campus-data accuracy
The official IIIT Bhopal annual report (2024–25) says academic activities are primarily conducted in the New Teaching Block and MPSTEP Building and reports 24 classrooms among the institute's facilities:
https://iiitbhopal.ac.in/Document/Important/Annual%20Report%202024-25%2013-03-2026%20Final_11zon.pdf

The initial room references (102, 103, NTB-TC-108(B), NTB-TC-206 and NTB-TD-208(B)) appear in an official first-semester timetable for Sept–Dec 2025:
https://iiitbhopal.ac.in/Document/Academic-2/TT%20-%201st%20Semester%20-%20All%20UG%20Course06092025-v5.pdf

That timetable is historical. These room references are therefore marked `Unknown` and their current allocation, capacity and timetable are NOT asserted. Ask the institute/authorized staff for current information and enter only verified details through Admin.

## Run locally
1. Extract the ZIP.
2. Open `index.html` in a modern browser.
3. Click **Admin**.
4. Demo password: `roomadmin26`.
5. Add or edit room records. Changes are stored in that browser's local storage.

## Personalise before publishing
Click **Edit details** on the homepage and enter the project details you are comfortable displaying. Avoid publishing a personal student identifier on a public link unless your instructor specifically requires it and you are comfortable with that exposure.

## Deploy free with GitHub Pages
1. Sign in to GitHub and create a new public repository, e.g. `classroom-finder`.
2. Upload `index.html`, `styles.css`, and `app.js` to the repository root. You may also upload the C source and README for assessment documentation.
3. Open repository **Settings → Pages**.
4. Under **Build and deployment**, choose **Deploy from a branch**.
5. Select branch `main` and folder `/ (root)`, then Save.
6. Wait for GitHub Pages to publish. The URL will look like `https://YOUR-USERNAME.github.io/classroom-finder/`.
7. Open the link in a private/incognito window and test all functions before submitting.

GitHub Pages documentation: https://docs.github.com/en/pages/quickstart

## Important limitations
- This is a front-end prototype. `localStorage` is device/browser-specific; admin edits do not sync to other students' devices.
- The demo password is visible in client-side JavaScript and is not secure authentication. Do not use real private data or claim it is a secure admin portal.
- No automatic timetable integration, room sensors, live occupancy detection or actual booking is implemented.
- For multi-user shared updates, use a hosted database (such as Supabase or Firebase) with server-side access controls and proper authentication. Do not put secret service keys in frontend code.

## Suggested demo flow
1. Open the student dashboard and search for `Room 102`.
2. Show that its status is initially `Needs update`.
3. Open Admin and sign in.
4. Edit a room, set a status and a last-checked time, then save.
5. Return to Find a room and show the updated status.
6. Explain that the current data is admin-entered and that verified live timetable integration is future scope.


## Timetable update (23 Nov 2026)
The room directory now includes the classroom and practical locations identified in the user's 12-page IIIT Bhopal first-year timetable for Sep-Dec 2026 (effective 01/09/2026): MPST-101/102/103/104, MPST NC-01/02/03/04, NTB TC-102/103, NTB TA-211, NTB TC-201, NTB TA-215(A), MPSTEP-116, MPSTEP-206, MPSTEP-117+118+105, MPSTEP Porch, Library and Sports area. Room names are based on the timetable's headers and individual lecture cells. The PDF does not provide room capacities or live occupancy. Some timetable pages instruct students to check each lecture cell for its assigned classroom, so do not interpret this directory as a guaranteed free-room schedule.


## Timetable-based availability (updated)
The dashboard includes day/time selectors and calculates occupied slots from explicit room assignments transcribed from the user's 12-page Sep–Dec 2026 timetable (effective 01/09/2026). Only clearly readable room/time entries are encoded. A room shown as “Vacant*” means no first-year booking is listed in the uploaded timetable for that slot; it is **not** a guarantee of campus-wide vacancy because other-year classes, bookings, maintenance, or unscheduled use are outside this source. Capacity is not specified in the timetable. Review the PDF pages referenced in the source before treating this as authoritative.

The admin dashboard is local-browser demo storage, not shared multi-user administration.
