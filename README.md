SJACS 即時電子報告版 (SJACS Instant Electronic Report Board)
This project provides a dynamic, real-time electronic display board designed for SJACS (St. Joseph's Anglo-Chinese School). It features rotating announcements, current time and date display, and an optional real-time bus ETA (Estimated Time of Arrival) display for nearby bus stops.

Features
Dynamic Announcements: Displays important school announcements and information fetched from a Google Sheet. The announcements rotate automatically with a smooth transition.
Real-time Clock & Date: Keeps track of the current time and date, displayed prominently.
Automatic Background Rotation: The background image changes periodically, offering a fresh visual experience.
Bus ETA Display: Integrates with local bus stop data to show real-time bus arrival estimates for "聖言巴士站" (Sing Yin Bus Stop) and "白虹樓巴士站" (Choi Hung Bus Stop). This feature is automatically shown during specific hours (15:45 to 22:00) and can also be toggled manually.
RSS News Feed: Displays a scrolling news ticker with local news updates from RTHK (Radio Television Hong Kong).
Auto-Refresh: The page automatically refreshes every 15 minutes to ensure the latest data and updates are loaded.

Getting Started
To run this project locally, simply clone the repository and open the index.html file in your web browser.
Bash
git clone https://github.com/your-username/your-repo-name.git
cd your-repo-name
open index.html


Dependencies
Google Fonts: Noto Sans HK and Oswald are used for typography, loaded directly from Google Fonts.
Google Sheets: The announcement data is pulled from a publicly accessible Google Sheet. You will need to update the SHEET_URL variable in the JavaScript to point to your own Google Sheet if you intend to use this for a different school or purpose. The sheet should be published to CSV format.
AllOrigins Proxy: Used to fetch RSS feed data due to cross-origin restrictions.
busetaSingYin.html and busetaChoiHung.html: These files are referenced for the bus ETA display. They are expected to contain the logic or iframes to display bus arrival times for the specified bus stops. These files are not included in this repository and would need to be created or provided separately.

Customization
Google Sheet Configuration
The announcements are loaded from a Google Sheet. To customize the announcements:
Create a Google Sheet with your desired announcement data.
Ensure the sheet is publicly accessible and published to CSV format.
Update the SHEET_URL variable in the script tag within index.html to your published CSV URL.
JavaScript
const SHEET_URL = 'YOUR_GOOGLE_SHEET_PUBLISHED_CSV_URL_HERE';


The script expects the announcement text in columns 2, 3, and 4, and the date in column 5 (zero-indexed).
Background Images
You can easily change the rotating background images by updating the backgroundImages array in the JavaScript:
JavaScript
const backgroundImages = [
    'URL_TO_YOUR_IMAGE_1.jpg',
    'URL_TO_YOUR_IMAGE_2.png',
    // Add more image URLs here
];


Bus ETA Files
The busetaSingYin.html and busetaChoiHung.html files are placeholders. You'll need to create these files and embed the relevant bus ETA widgets or content for your specific bus stops.
Styling
All styling is managed within the <style> tags in the index.html file. You can modify the CSS to change colors, fonts, sizes, and layout to match your branding.

License
This project is open-source and available under the MIT License. Feel free to use, modify, and distribute it as you see fit.

Contributing
Contributions are welcome! If you have suggestions for improvements, bug fixes, or new features, please open an issue or submit a pull request.

Acknowledgments
Google Fonts for beautiful typography.
AllOrigins for the cross-origin proxy service.

Feel free to reach out if you have any questions or need assistance!
