# About NomPy
NomPy is an application designed to search for free food events by parsing data from RSS feeds. The program creates an html file that displays the results as a map and table on a webpage. The results are also exported as calendar events and a CSV summary to the current directory. Users can choose to run the program from a Python interpreter or from the exexcutable file. The latest release for all the code can be downloaded by clicking 'Release' on the repository page. 

## User Inputs
### Input GUI
After running NomPy, the user will first encounter a graphical interface to set the preferences for the event search. The user has the option of adding additional search terms as well as new RSS feeds. 
#### Adding a new RSS Feed:
The user can add a new RSS feed to the search by providing the link to the feed (click "Subscribe to Feed"), not the hosting page itself.

### Mapbox Capability
The map plotting functionality requires a Mapbox account to be enabled (sign up here https://account.mapbox.com/auth/signup/). After creating an account, the user can copy the default public token in the account homepage. The access token can be pasted into the interface that opens in order to enable map plotting. Alternatively, if the user does not wish to create a Mapbox account, an option to display the table results only can be selected.

## Outputs
While the program is running, the total number of calendar events found will be displayed on the console. When it is finished, an html page containing a map (if enabled) and table of the results will open in the user's browser. Another interface will be generated to allow the user to filter the results by date and food type and replot the filtered results. __***Exiting the filter GUI is necessary to end the program***__ The filter GUI can be exited by clicking 'Cancel' or the exit icon in the upper right corner.

# How to use NomPy
NomPy has the option of being run through a Python interpreter or by using the bundled NomPy.exe file.
## From Source:
Download all files in the 'NomPy_Source' folder from the GitHub respository and install the required packages.

For conda
```
conda install --file requirements.txt
```

For pip
```
pip install -r requirements.txt
```
Navigate to the nomPy Source directory and start the program by running 'NomPy.py'. Use the GUI that pops up to set preferences. The map and table will open in your default browser.

## From executable:
Download and extract the 'NomPy.Application.zip' file from the latest release, and run 'NomPy.exe'. *Note:* the application will not work unless 'NomPy.exe' is kept in the containing folder created when it is unzipped. If you would like to move the file, please create a shortcut that links to the original.

# Compatible RSS Feeds
NomPy supports feeds hosted by:
* Localist
* Trumbo

NomPy may work for other feeds, but is tailored for the listed feeds. 

# Troubleshooting
## I need to change my Mapbox access token, but the GUI isn't showing up
Delete the 'config.json' file from your directory and re-run NomPy. NomPy searches the current directory for the config file (where the Mapbox token is stored), and loads the token if it is there. The GUI will not show up if the file exists in the directory.

## I am getting a strange error, and the user Initial Settings GUI won't show up
Make sure all blank (tkinter) windows are closed and re-run NomPy. This can happen the files are not downloaded properly and an extra GUI window fails to get destroyed. Make sure all necessary files are in the same direcotry (including 'dotnom.png'), and try again.

## What are the required packages and versions needed to run the source code?
The 'requirements.txt' file contains a list of the packages used in NomPy with their respective versions. See the above section 'How to Use NomPy' => 'From Source' for installation instructions via *pip* and *conda.*

Happy Eating!
