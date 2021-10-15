######################
# Prior Requirements #
######################
- Hardware: Access via computer (Microsoft Windows)
- Software: UiPath Web Automation Extension, UiPath Software License, Microsoft Excel Spreadsheet Software, Chrome Extension, Microsoft Windows
- Website: Access via URL
  - IMDb: https://www.imdb.com/
  - Box Office Mojo: https://www.boxofficemojo.com/
- Make sure that the Chrome Extension is enabled
  - Open UiPath software on computer → Go to ‘Tools’ page → Under UiPath Extensions, select Chrome → A dialog box confirming the extension will be displayed (Now the extension is installed)  → If not already, close all Chrome browsers → Go to Chrome page → In the Google Chrome confirmation pop-up, click ‘Enable Extension’ (Now the extension is enabled)
- Ensure that 'Trust access to the VBA project object model' is checked on Excel
  - Open a new Excel workbook →  File →  Options →  Trust Center →  Macro Settings →  Under Developer Macro Settings, check 'Trust access to the VBA project object model'


# User Manual for MovieSearch (Steps/Instructions)
  1. Download the MovieSearch zip file
  2. Open UiPath Studio and click 'Open a Local Project'
  3. Select 'project.json' file
  4. Click 'Project' under the project tab on the main page
  5. Select the 'Main.xaml' file and run the software
  6. As it executes, it will prompt the user to select the desired month
      - Displays 'Please select the month' with list of months in a drop-down menu
  7. Select the preferred month and select ‘Ok’
      - It will takes some time running the bot (approximately 5 minutes)
  8. While executing, the bot will direct to the Box Office Mojo website and IMDb website performing parallel activity
  9. Once the bot has finished running, movie information for the selected month will be stored in Excel file.


# Limitations
- The bot might not execute if two websites', boxofficemojo and IMDb, servers are down. If this is the case, try running the bot again after a few minutes.
- Comes under exceptional handling:	
    - There are some cases the bot will pick up on multiple movies directed by one director that were released in the same month. - consequently we decided to include them all but order them by their ranking order (Highest gross first).
    - The movies which have the same title can confuse the bot as it will include the same details of the production team and distributor - Users may need to manually search for the movie titles that do release in the same month with the same title, and manipulate the data to have the correct corresponding details across the films.

