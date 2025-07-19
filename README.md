# SJACS 即時電子報告版 (SJACS Instant Electronic Report Board)

This project provides a dynamic, real-time electronic display board designed for SJACS (St. Joseph's Anglo-Chinese School). It features rotating announcements, current time and date display, and an optional real-time bus ETA (Estimated Time of Arrival) display for nearby bus stops.

---

## Features

* **Dynamic Announcements:** Displays important school announcements and information fetched from a Google Sheet. The announcements rotate automatically with a smooth transition.
* **Real-time Clock & Date:** Keeps track of the current time and date, displayed prominently.
* **Automatic Background Rotation:** The background image changes periodically, offering a fresh visual experience.
* **Bus ETA Display:** Integrates with local bus stop data to show real-time bus arrival estimates for "聖言巴士站" (Sing Yin Bus Stop) and "白虹樓巴士站" (Choi Hung Bus Stop). This feature is automatically shown during specific hours (15:45 to 22:00) and can also be toggled manually.
* **RSS News Feed:** Displays a scrolling news ticker with local news updates from RTHK (Radio Television Hong Kong).
* **Auto-Refresh:** The page automatically refreshes every 15 minutes to ensure the latest data and updates are loaded.

---

## Getting Started

To run this project locally, simply clone the repository and open the `index.html` file in your web browser.

```bash
git clone https://github.com/ltmtms/signage
cd signage
open index.html
