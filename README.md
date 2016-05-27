# ORMAP - Map Production Toolbar

The ORMAP Map Production toolbar is a specific set of tools built to support Oregon Counties and the mapping requirments set forth by the Oregon Department of Revenue for mapping tax 
parcels.  The tools are built using the programming language Python and the [ESRI](https://esri.com) ArcPy python library.  They are  platform as an Add-in and supports version 10.1+ (currently tested up to version 10.3). ArcMap is required 
to use this toolbar. 

![alt text](https://raw.github.com/ORMAPtools/MapProduction/Supplimental/Toolbar.png "Image of the toolbar")


### Download
The download contains everything you need including the Add-In, documentation, and configuration files.
> [DOWNLOAD NOW](https://raw.github.com/ORMAPtools/MapProduction/Ormap+Map+Production+AddIn.zip).


### Documentation/Configuration

This Add-In requires configuration and setup prior to use.  This documentation is meant for an administrator who will configure and distribute the Add-In to users.   

Download the zip file and unzip it to a folder on your hard drive.  We can use one of the buttons on the toolbar to help us configure the map elements for the new toolbar.  First, create and install the toolbar.

1.	Start by creating the Add-In file.  To do this, navigate to where you unzipped the contents of the zip file and go into the AddIn folder.  
2.	Double click the makeaddin.py file to create an Add-In.  You should see a file created called Ormap Map Production.esriaddin. 
3.	Double click this file and click Install Add-In to install into ArcMap.   
4.	Open your Map Production map document (mxd).  In ArcMap, click Customize >> Add-In Manager.  Ensure you are on the Add-Ins tab and verify that the toolbar is installed. 

You can now use the Page Layout Element Report to see what map element names we currently have and compare them to what the names should be for use in the new toolbar.

1.	Verify the new Ormap Map Production toolbar is turned on.  In Arcmap, click Customize >> Toolbars.  Scroll through the list and make sure the Ormap Map Production Toolbar has a check next to it.  If it does not click it to turn it on. 
2.	Hover your mouse over each tool on the toolbar to find the Page Layout Element Report tool.  Click this tool, specify an output for the report and press Ok.  
3.	When the report is finished it should open automatically.  This report will contain the names and locations of the map elements on your page.  These will likely need to be renamed in order for use with the new toolbar.   It is recommended that you make a backup copy of your Map Production map document (mxd) prior to making these changes.  

The following is a list of map elements for the new toolbar.  Those denoted in bold are required.  The others are optional for use in the toolbar.  Your county may contain a few or all of these elements.  

+	MainDF = The main dataframe.
+	MapNumber* = Not used on the map, however it is used by the code to determine which map you are working with.
+	MainMapTitle* = Map title.
+	CountyName** = The County name.
+	MainMapScale** = The map scale in the format 1” = x’
+	Disclaimer* = The maps disclaimer.
+	DisclaimerBox** = A box that surrounds the disclaimer.
+   PlotDate* = The auto generated date on the map.
+	CanMapNumber* = The cancelled numbers primary column.
+	Can MapNumber2** = A second column for cancelled numbers overflow.
+	CanMapNumber3** = A third column for cancelled numbers overflow.
+	UpperRightMapNum* = The mapnumber listed in the upper right corner of the map.
+	LowerRightMapNum* = The mapnumber listed in the lower right corner of the map.
+	UpperLeftMapNum*** = The mapnumber listed in the upper left spot.
+	LowerLeftMapNum*** = The mapnumber listed in the lower left spot.
+	LocatorDF = The locator data frame.
+	SectionsDF = The Sections data frame.
+	QSectionsDF = The Quarter Sections data frame.
+	smallMapTitle*** = A smaller version of the MainMapTitle.
+	smallMapScale*** = A smaller version of the MainMapScale.
+	NorthArrow* = The North arrow.
+	ScaleBar* = The scalebar.

\* These items have their x/y coordinates stored in the PageLayoutElements table.  
\** These items x/y coordinates derived from other page elements. These may include offsets described in the configuration files.  
\***  These items x/y coordinates are not stored or calculated however the text value is repeated from another page element.  

The download contains diagrams displaying the map elements as they might appear on the map.  There are two examples, one for 18x20 and another for 18x24:


### Issues
Find a bug or want to request a new feature?  Please let us know by submitting an [issue](https://github.com/ORMAPtools/MapProduction/issues). 


### Credit/Contributions
The ORMAP tools were created by the ORMAP tools developers.  We encourage anyone to help contribute to the ORMAP tools project.  Please submit an [issue](https://github.com/ORMAPtools/MapProduction/issues) or fork and create a pull request.


### Licensing
Licensed under the GNU General Public License, version 3 (GPL-3.0).  
> [View License](https://github.com/ORMAPtools/MapProduction/blob/master/LICENSE).