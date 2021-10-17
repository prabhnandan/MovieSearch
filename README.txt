# Prior Requirements
- Hardware: Access via computer (Microsoft Windows)
- Software: UiPath Web Automation Extension, UiPath Software License, Microsoft Excel Spreadsheet Software, Google Chrome, Chrome Extension, Microsoft Windows
- Website: Access via URL
  - IMDb: https://www.imdb.com/
  - Box Office Mojo: https://www.boxofficemojo.com/
- Make sure that the Chrome Extension is enabled
  - Open UiPath software on computer → Go to ‘Tools’ page → Under UiPath Extensions, select Chrome → A dialog box confirming the extension will be displayed (Now the extension is installed)  → If not already, close all Chrome browsers → Go to Chrome page → In the Google Chrome confirmation pop-up, click ‘Enable Extension’ (Now the extension is enabled)
- Ensure that 'Trust access to the VBA project object model' is checked on Excel
  - Open a new Excel workbook →  File →  Options →  Trust Center →  Macro Settings →  Under Developer Macro Settings, check 'Trust access to the VBA project object model'
- Ensure ExportMovies.xlsx and Historic.xlsx are present in the folder


# User Manual for MovieSearch (Steps/Instructions)
  1. Download the MovieSearch zip file
  2. Open UiPath Studio and click 'Open a Local Project'
  3. Select 'project.json' file
  4. Click 'Project' under the project tab on the main page
  5. Select the 'MovieSearch.xaml' file and run the software
  6. As it executes, it will prompt the user to select the desired month
      - Displays 'Please select the month' with list of months in a drop-down menu
  7. Select the preferred month and select ‘Ok’
  8. Type the year you want to consider, it will default to the current year
      - Select 'Ok' when the message box contains the right year
  10. While executing, the bot will direct to the Box Office Mojo website and IMDb website performing parallel activity
  11. Once the bot has finished running, movie information for the selected month will be stored in Excel file.


# Limitations
- The bot might not execute if any of the two websites', boxofficemojo and IMDb, servers are down. If this is the case, try running the bot again after a few minutes.
- URL dependant, if they remain consistent then the automation will be able to run without any errors, however if Boxofficemojo or IMDb were to change then the bot may not be able to register the changes.
- The bot always selects the first movie in the search performed on IMDb website. If there are multiple movies with the same name, the incorrect movie might get selected - Users may need to manually manipulate the data to have the correct corresponding details across the films. (The client has agreed to ignore this limitation)

# Logging
- The solution automatically logs certain steps while its running to show the progress and if any errors occur. This can be viewed within the UiPath 'Output' terminal at the bottom of the screeb, but it is also written to the default UiPath logging location, and can be viewed and analysed later if needed.
- The default logging location will depend on your operating system username, but on a Windows machine it should be located at `C:\Users\{Your Username}\AppData\Local\UiPath\Logs`.  
- The file should be called `{Date of run}_Execution.log` and all log messages that were in the UiPath 'Output' terminal will be saved here automatically.
