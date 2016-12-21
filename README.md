# Rhino2Revit
Use this workflow to import Rhino geometry into Revit as native geometry.




# Links To Additional Material:

Autodesk Univiersity 2016 Class
http://au.autodesk.com/au-online/classes-on-demand/class-catalog/2016/revit-architecture/ar21124

box link to class material
https://perkinswill.box.com/v/AU2016-AR21124


SF Dynamo User Group Recording:
http://sfdug.blogspot.com/2016/01/sfdug-february-2016-meeting-what-revit.html

#Support:
Dynamo version: 1.2
Revit version: 2015, 2016, 2017
Required Packages: Spring Nodes
Last Update: 2016.12.08

Author: Jeremy Luebker

# Instructions:
Step 1)	Make sure your Rhino geometry are all 	close polysurface (extrusions such as boxes 	or cylinders do not currently work with this 	method).

Step 2) 	Export the geomety as an .SAT file, make 	sure your file units are in Feet.

Step 3)	Use the input browse node to navigate and 	select the SAT file.

Step 4) 	To execute the import, hit the RUN button 	in the lower left corner of the Dynamo 	screen. 

Step 5) 	Change Default Form Material to have a 	poche color and solid fill: in Revit, Manage 	> Materials > Graphics

Step 6) Set the Default Form material to be the default material for the Generic Model Category: in Revit, Manage > Object Styles > Generic Model > Material


*** NOTE: If you are importing many solids, it may take a little while to import each, so be patient.


# Notes:
This workflow is still very much a work-in-progress and my not work every time. Even if all your Rhino geometry is completely water-tight, they still may not import correctly (it has happened but not often).

Every solid in the SAT will be imported as a seperate Revit family. Solids can be joined into one family, however, the best practice would be to boolean-union the elements into one solid in rhino before importing.

