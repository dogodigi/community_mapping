# The iD Editor
source: [learnosm.org](http://learnosm.org/en/beginner/id-editor/)

The iD editor is one of the OpenStreetMap editors. You can run it in the browser from the OpenStreetMap website. It allows mapping from various data sources such as satellite and aerial imagery, recorded GPS tracks, [Field Papers](http://fieldpapers.org) or [Mapillary](https://www.mapillary.com). 

## Starting the iD Editor

- The iD editor requires an active connection to the Internet.  
- Open your Internet browser, and go to the OpenStreetMap website at [http://www.openstreetmap.org](http://www.openstreetmap.org).  
- **Login** using your OpenStreetMap account  
- Pan and zoom the map to the area that you wish to edit. You can pan by holding the left mouse button and dragging the map to your desired area.  
- Click on the small arrow next to **Edit**. Then click **Edit with iD (in-browser editor)**.  

![image1][]

## Graphical User Interface

![image2][]

On the **Edit Feature (1)** panel, you can show, edit or enter details about the objects on the map (tags). In the **Tools (2)** section, you find everything you need to draw, or undo drawing. With the **Map control (3)** you can change the appearance of the map, add or alter layers and open documentation. The **Information panel (4)** shows scale, contributors and version number of the iD editor.



| Function | Shortcut |  |
| -- | -- | -- |
| Draw Point (node) | 1 | ![image3][] |
| Draw Line (way) | 2 | ![image4][] |
| Draw Area (way) | 3 | ![image5][] |
| Undo | Ctrl + z | ![image6][] |
| Redo | Ctrl + y | ![image7][] |
| Save changes | Ctrl + s | ![image8][] |
| Zoom In | + | ![image9][] |
| Zoom Out | - | ![image10][] |
| Show my location |  | ![image11][] |
| Configure background |  | ![image12][] |
| Mapdata | f | ![Map Data][] |
| Help menu | h | ![image13][] |

### Configuring the Background Layer

Click the **Background settings** button or use the *shortcut key* **b**.![image14][]{: height="24px"}  
![image15][]  
To change the **brightness level** click one of these boxes, the levels are 100%, 75%, 50%, and 25% ![image16][]{: height="24px"}  
You also can **change the background layer** based on your desired tile provider (the default is Bing Aerial Imagery).  

You can add your own map tiles by clicking on **Custom**. For example, if you want to **add a Field Paper** [^fieldpaper], click **Custom** then click on the magnifying glass (search) icon to open the following window:-  
![image17][]   
and enter your **FieldPaper snapshot URL**, which will be something like this: <http://fieldpapers.org/snapshot.php?id=cqhmf2v9#18/37.80593/-122.22715>   
To **display GPS tracks from your computer** (GPX format), drag and drop the GPX file into iD editor.  
To enable **OpenStreetMap GPS traces** click on the box. In the image below, public GPS traces are shown in various colors, indicating the direction of travel.  
![osm gps traces][]  
If there is [imagery offset](/en/josm/aerial-imagery), you can **correct the imagery offset** by clicking **Fix Alignment**. ![image18][]  

- Click the navigation buttons to move the imagery. Click the reset button to return to the default position. ![image20][]  

Basic Editing with iD  
----------------------  

### Adding Points  

To add a new point, click on the **Point** button. ![image3][]{: height="24px"}  

- Your mouse cursor will change into plus (+) sign. Now, click on a position that you know to mark a location. For example, if you know that there is a hospital in your area, click on the position of the hospital building.  
![image21][]  
- Notice that a new point is added. At the same time, the left panel will change to show a form where you can select attributes for the object. Click **Hospital Grounds** to tag the point as a hospital.  
![image22][]  
- You can use the forms to fill detail information about your point. You can fill hospital name, address, and/or other additional information. Note that each feature will have different options, depending on what tag you choose from the feature panel.  
- If you make a mistake, such as a wrong location, you can move your point to a new location by holding the left mouse button on your point and dragging it. Or, if you want to delete your point, click the left mouse button on the point and then click the button which looks like a trashcan. ![image23][]{: height="24px"}  
A "point" created in the iD editor is actually a standalone "node" with a set of "tags" on it.  

### Drawing Lines  

To add a new line, click on the **Line** button. ![image4][]{: height="24px"}  

- Your mouse cursor will change into plus (+) sign. Find a road that hasn’t been drawn on the map and trace it. Click once on a point where the road segment begins, move your mouse, and click to add additional points. Double-click to end the drawing process. Notice the panel on the left.  
![image24][]  
- Just as with a point, select the appropriate tags for your line.  
- You can drag points from the line by clicking your left mouse button on a point and dragging it.  
- You also can move the whole line by selecting it, and choosing the **Move tool**. Then drag the line to a new position. ![image30][]{: height="24px"}  
- When you click your left mouse button on an individual point (node) on the line, you will see these tools:  
- Delete point from line. ![image23][]{: height="24px"}  
- Disconnect point from line. ![image26][]{: height="24px"}  
- Split a line into two lines from the point you’ve selected. ![image27][]{: height="24px"}  
- When you click your left mouse button on a line (but not on a point), you will see these tools:  
-   Delete line. ![image23][]{: height="24px"}  
-   Create a circle from a line (only active if the line is closed) ![image29][]{: height="24px"}  
-   Move line ![image30][]{: height="24px"}  
-   Form a square shape from a line (only active if the line is closed) ![image31][]{: height="24px"}  
-   Reverse line direction (good for rivers & one-way streets) ![image32][]{: height="24px"}  

A "line" created in the iD editor is actually a "way" with "tags" on it.

>A special note about **Deleting**: In general you should avoid deleting other people's mapping if it just needs improvement. You can delete your own mistakes, but you should try to *adjust* other people's mapped objects if they need changes. This preserves the history of the items in the OSM database and is respectful of fellow mappers. If you really feel something should be deleted, consider asking the original mapper or one of the OSM email lists about it first.

### Drawing Shapes (Polygons)

To add a new multi-sided shape, click on the **Area** button. ![image34][]{: height="24px"}  

- Your mouse cursor will change into plus (+) sign. Try to trace a building using the imagery as a guide.  
- You will notice that the color of your shape will change depending on the attributes that you assign to it.  
![image35][]  
- The tools that are available when you select a shape are similar to those when you click on a line.  

A "polygon" in the iD editor is actually a "closed way" with tags on it.

Saving Your Changes
--------------------

When (and if) you want to save your edits to OpenStreetMap, click the **Save** button. The panel on the left will show the upload panel.  
![image36][]  

- Enter a comment about your edits and click **Save**.  

> If you have edited the same feature (point, way or area) at the same time as another person was editing it, you will receive a warning that your edits cannot be uploaded until you have resolved the **conflicts** - choose whose edits to accept & upload your changes. *Resolving conflicts often involves accepting the other persons edits, in which case you will probably wish to return to the feature in question and edit again (**this time save soon after the edit to try to avoid a conflict again!**).*

Additional Information and Custom Tags
---------------------------------------

When you are editing an object, you will see a strip of icons at the bottom of the attribute panel. You can add additional information by clicking these icons:

- Add elevation ![image37][]{: height="24px"}  
- Add notes ![image38][]{: height="24px"}  
- Add contacts / phone number ![image39][]{: height="24px"}  
- Add source tag ![image40][]{: height="24px"}  
- Add website ![image41][]{: height="24px"}  
- Add accessibility information ![image42][]{: height="24px"}  
- Add Wikipedia link ![image43][]{: height="24px"}  

Or, you can add custom tags by clicking **All tags**. ![image44][]{: height="24px"}  

- This will show all the tags attached to the feature.  
![image45][]  
- Click the plus sign (+) to add keys and values or click the trash icon to delete tags.

iD versus JOSM
---------------  

**iD is good for...**

- When you are doing simple edits  
- When you have fast Internet to load the imagery and save the edits  
- When you want to be sure to follow a consistent and simple tagging scheme  
- When you are restricted from installing a program on the computer you are using

**JOSM is better...**

- When you are adding many buildings (See buildings_tool plugin)
- When you are editing many polygons or lines that already exist
- When you are on an unreliable Internet connection or offline
- When you are using a specific tagging scheme (or custom presets)

[^fieldpaper]: There is a [section of LearnOSM](/en/mobile-mapping/field-papers/) giving more information about Field Papers.
[image1]: http://www.learnosm.org/images/beginner/id-editor_image1.png 
[image2]: http://www.learnosm.org/images/beginner/id-editor_image2.png
[image3]: http://www.learnosm.org/images/beginner/id-editor_image3.png
[image4]: http://www.learnosm.org/images/beginner/id-editor_image4.png
[image5]: http://www.learnosm.org/images/beginner/id-editor_image5.png
[image6]: http://www.learnosm.org/images/beginner/id-editor_image6.png
[image7]: http://www.learnosm.org/images/beginner/id-editor_image7.png
[image8]: http://www.learnosm.org/images/beginner/id-editor_image8.png
[image9]: http://www.learnosm.org/images/beginner/id-editor_image9.png
[image10]: http://www.learnosm.org/images/beginner/id-editor_image10.png
[image11]: http://www.learnosm.org/images/beginner/id-editor_image11.png
[image12]: http://www.learnosm.org/images/beginner/id-editor_image12.png
[Map Data]: http://www.learnosm.org/images/beginner/id-editor_map_data.png
[image13]: http://www.learnosm.org/images/beginner/id-editor_image13.png
[image14]: http://www.learnosm.org/images/beginner/id-editor_image14.png
[image15]: http://www.learnosm.org/images/beginner/id-editor_image15.png
[image16]: http://www.learnosm.org/images/beginner/id-editor_image16.png
[image17]: http://www.learnosm.org/images/beginner/id-editor_image17.png
[image18]: http://www.learnosm.org/images/beginner/id-editor_image18.png
[image19]: http://www.learnosm.org/images/beginner/id-editor_image19.png
[image20]: http://www.learnosm.org/images/beginner/id-editor_image20.png
[image21]: http://www.learnosm.org/images/beginner/id-editor_image21.png
[image22]: http://www.learnosm.org/images/beginner/id-editor_image22.png
[image23]: http://www.learnosm.org/images/beginner/id-editor_image23.png
[image24]: http://www.learnosm.org/images/beginner/id-editor_image24.png
[image25]: http://www.learnosm.org/images/beginner/id-editor_image25.png
[image26]: http://www.learnosm.org/images/beginner/id-editor_image26.png
[image27]: http://www.learnosm.org/images/beginner/id-editor_image27.png
[image28]: http://www.learnosm.org/images/beginner/id-editor_image28.png
[image29]: http://www.learnosm.org/images/beginner/id-editor_image29.png
[image30]: http://www.learnosm.org/images/beginner/id-editor_image30.png
[image31]: http://www.learnosm.org/images/beginner/id-editor_image31.png
[image32]: http://www.learnosm.org/images/beginner/id-editor_image32.png
[image33]: http://www.learnosm.org/images/beginner/id-editor_image33.png
[image34]: http://www.learnosm.org/images/beginner/id-editor_image34.png
[image35]: http://www.learnosm.org/images/beginner/id-editor_image35.png
[image36]: http://www.learnosm.org/images/beginner/id-editor_image36.png
[image37]: http://www.learnosm.org/images/beginner/id-editor_image37.png
[image38]: http://www.learnosm.org/images/beginner/id-editor_image38.png
[image39]: http://www.learnosm.org/images/beginner/id-editor_image39.png
[image40]: http://www.learnosm.org/images/beginner/id-editor_image40.png
[image41]: http://www.learnosm.org/images/beginner/id-editor_image41.png
[image42]: http://www.learnosm.org/images/beginner/id-editor_image42.png
[image43]: http://www.learnosm.org/images/beginner/id-editor_image43.png
[image44]: http://www.learnosm.org/images/beginner/id-editor_image44.png
[image45]: http://www.learnosm.org/images/beginner/id-editor_image45.png
[osm gps traces]: http://www.learnosm.org/images/beginner/id-editor_gps_public.png
