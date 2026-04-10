School-Log-Archiver
A GUI tool that automatically scrapes and archives weekly newsletters from the Manbang School parent portal, saving them as PDFs, images, HTML, and plain text — organized by semester and week.

Features

Automated Scraping — Uses Selenium WebDriver to automatically crawl the weekly newsletter pages
PDF Export — Converts scraped newsletters and images into PDF files
Image Export — Saves image files separately
HTML Export — Saves raw HTML just in case
Text Export — Saves plain text just in case
Auto Folder Organization — Files are automatically sorted by semester and week into the weekly_notices folder


Getting Started
Option 1 — Run the prebuilt executable (recommended)

Go to the latest release page and download the following files into the same folder:

gui_app.exe
chromedriver.exe — must match your installed Chrome version (download here). The bundled one should work in most cases.


Double-click gui_app.exe to launch.

Option 2 — Run from source (for developers)

Install Python 3.8+
Install dependencies:

bash   pip install -r requirements.txt
If requirements.txt is missing, install manually:
bash   pip install selenium fpdf requests

Place chromedriver.exe (matching your Chrome version) in the project root folder.
Run the app:

bash   python gui_app.py

Usage

Launch gui_app.exe (or python gui_app.py) — a GUI window will appear.
Log in:

Click the "Log In" button — a new Chrome window will open.
Manually log in to the Manbang School parent portal.
Once logged in and the newsletter page loads, the GUI status will change to "Logged In".


Start archiving:

In the Chrome window, select the year and semester you want to archive.
Click the "Start" button in the GUI.
The app will automatically scrape all weekly newsletters for the selected semester and save them to the weekly_notices folder. Progress is shown in the status bar.


Stop archiving — Click the "Stop" button at any time to pause scraping.
Open saved folder — Click "Open Saved Folder" to open the weekly_notices directory directly.


Troubleshooting

chromedriver.exe errors:

The chromedriver.exe version must match your installed Chrome browser version.
If you've updated Chrome, download a matching chromedriver.exe from the ChromeDriver download page.
Make sure gui_app.exe and chromedriver.exe are in the same folder.


Scraping stops working:

If the Manbang School parent portal updates its HTML structure, the scraper may break. In that case, the source code (script.py) will need to be updated manually.
