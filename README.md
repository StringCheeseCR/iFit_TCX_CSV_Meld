# iFit_TCX_CSV_Meld
Melding TCX &amp; CSV files for iFit workouts

Note that you only need the one file (iFit.R).  The other files are just convenient for me to associate them here.

Installation
1. Download R from https://cran.r-project.org/
2. Run the installer
3. Open the RGui program
4. In the RGui program go to the Packages menu
   A. Click Install Packages...
   B. Choose the location nearest to you
   C. Install the following packages...
      1. data.table
      2. zoo
      3. XML
      4. lubridate
      5. stringr
      
      Note: you may need to install 1 at a time.
5. Now open the iFit.R file in the RGui
6. Copy the entire contents of the iFit.R file
7. Click the "Window" button at the top to return to the console
8. Paste the text that you copied

Creating the better TCX file
1. In iFit download both the TCX and CSV with Elevation files and put them into the same directory.
2. Run the command to create the better TCX file

    a <- meld_iFit_S22i_CSV_TCX_to_better_TCX(chr.file = 'filename without extension', chr.path = 'directory files are in')
   
    ex. a <- meld_iFit_S22i_CSV_TCX_to_better_TCX(chr.file = '2021_03_05_19_03_Playa_Guiones_Interval_Walk,_Costa_Rica', chr.path = 'C:\\iFit\\')
    
    Note: If the filename contains "Ride" then the Activity will be set to "Biking" in the tcx file, otherwise it defaults to "Running"
    
3. Upload the file that ends in better to Garmin/Strava


