# The basics of geodata

## Summary
Attendees will learn to **think in models**. They gather insight on what spatial data is, how it is collected and how it relates to regular data. After this day, they will have good insight on how to model real-world objects as data.

----

## Models
A real-world object cannot be stored on a computer, we store "a representation of a real-world object that matches our requirements". What can such requirements be? Basically it is all about being useful. Models form the building blocks that help us make decisions, draw conclusions and get things done.

> ##### Excercise 1
Imagine your company doing paint jobs. It is your job to go paint the interior walls of a building. What would you need to model? What do you need to store on a computer so you can calculate the ammount of paint required and the number of hours your workers are going to spend to paint all the walls?

> ##### Excercise 2
You are a calculator with a road-construction company. What do you need to store on a computer so you can calculate how much asphalt is required? And how about the speed? What do you need to know to determine the maximum speed that can be driven on the road?

> ##### Exercise 4
You own a public pool. What information do you need to store to attract visitors? And do you need other information from other parties?

We now have some insight in what models are. You now know that often models with information about size, shape and location can greatly enhance the possibilities to use them.

## Geometry

So you learned about walls, the shape of roads and location. Geometry is the branch of mathematics concerned with questions of shape, size, relative position of figures, and the properties of space. When we talk about this in general, we will from now on address this as __Geometry__. Geometry and geometric calculations require study. In this course the explaination of geometry will be limited to what is required to reach the goals of the training.

This table shows our geometry primitives. We will discuss them in a more detail. If you want to know more, the table contains links to wikipedia and openstreetmap that provide information about the different primitives.

| Wikipedia |  | Math | Openstreetmap |
| -- | -- | -- | -- |
| [Point](https://en.wikipedia.org/wiki/Point_%28geometry%29) | ![](https://upload.wikimedia.org/wikipedia/commons/c/c2/SFA_Point.svg) |  [X, Y] | [Node](http://wiki.openstreetmap.org/wiki/Node) |
| [LineString](https://en.wikipedia.org/wiki/Line_segment) | ![](https://upload.wikimedia.org/wikipedia/commons/b/b9/SFA_LineString.svg) |  [[X1, Y1], [X2, Y2] .. [Xn, Yn]] | [Way](http://wiki.openstreetmap.org/wiki/Way) |
| [Polygon](https://en.wikipedia.org/wiki/Line_segment) | ![](https://upload.wikimedia.org/wikipedia/commons/3/3f/SFA_Polygon.svg) |  [[X1, Y1], [X2, Y2][ Xn, Yn]..[__X1__,__Y1__]] | [Way](http://wiki.openstreetmap.org/wiki/Way) |
| [Polygon with hole](https://en.wikipedia.org/wiki/Line_segment) | ![](https://upload.wikimedia.org/wikipedia/commons/5/55/SFA_Polygon_with_hole.svg) |  [[[X1, Y1], [X2, Y2][ Xn, Yn]..[__X1__,__Y1__]],[[X1, Y1], [X2, Y2][ Xn, Yn]..[__X1__,__Y1__]]],  | [Relation](http://wiki.openstreetmap.org/wiki/Relation) |

### Points
A point is a geometry primitive. A point can be modelled by an ordered pair (x,y) or (latitude,longitude) or triplet (x,y,z) or (latitude, longitude, height). There are more representations, for the purpose of this course, we will stick with (x,y) 2 dimensional coordinates. Feel free to get yourself informed about 3D after this course, it opens a whole new world of opportunities! In OpenStreetMap a point is called a _node_.

| Type |  |  | Openstreetmap |
| -- | -- | -- | -- |
| [Point](https://en.wikipedia.org/wiki/Point_%28geometry%29) | ![](https://upload.wikimedia.org/wikipedia/commons/c/c2/SFA_Point.svg) |  [X, Y] | [Node](http://wiki.openstreetmap.org/wiki/Node) |


 A point tells you something about location, but hardly about shape. So when we model a building as a point and want to use it to calculate a paint job, it will not do. Points alone hardly tell us anything. It is __relative position__ that makes it shine!


> ##### Exercise 5
When we have a point in (latitude, longitude) that represents a restaurant and a point that represents our current position, what can we do with that?

> ##### Exercise 6
When we have a point in (latitude, longitude) that represents an explosion and we have a lot of points that represent people, what can we do?

### Lines
Lines, we all know what they are. In mathematics, they are often defined as a function (vectors). But in computer systems, they are most often a collection of points and that is often also how they are stored in the database. The lines computers need are constructed out of points. Lines can also be connected. From lines we can calculate length. Lines also form the basics for navigation. In OpenStreetMap a line is called a _way_.

| Type |  |  | Openstreetmap |
| -- | -- | -- | -- |
| [LineString](https://en.wikipedia.org/wiki/Line_segment) | ![](https://upload.wikimedia.org/wikipedia/commons/b/b9/SFA_LineString.svg) |  [[X1, Y1], [X2, Y2] .. [Xn, Yn]] | [Way](http://wiki.openstreetmap.org/wiki/Way) |


> ##### Exercise 7
Why are lines used for navigation and why is that better then using points?

> ##### Exercise 8
We have a line representing a planned road and a line representing a river. These lines cross. What does this inform us about?
 

### Polygons
As you may have noticed by now, primitives are constructed from other primitives. Lines are constructed from points. A polygon is a closed shape. It is constructed from lines. The fact that the first point is exactly the same as the last one tells the computer that it is __closed__. So a polygon is a collection of lines, where the sequence is important and the first point is __exactly__ the same as the last one.

In Openstreetmap a polygon is a called a _way_, but this time the first and last point on the way need to be connected!

| Type |  |  | Openstreetmap |
| -- | -- | -- | -- |
| [Polygon](https://en.wikipedia.org/wiki/Line_segment) | ![](https://upload.wikimedia.org/wikipedia/commons/3/3f/SFA_Polygon.svg) |  [[X1, Y1], [X2, Y2][ Xn, Yn]..[__X1__,__Y1__]] | [Way](http://wiki.openstreetmap.org/wiki/Way) |

Polygons can also have holes in them. In the database these are modelled by adding more polygons that act as inverse. In OpenStreetMap, these are modelled through _relations_.

| Type |  |  | Openstreetmap |
| -- | -- | -- | -- |
| [Polygon with hole](https://en.wikipedia.org/wiki/Line_segment) | ![](https://upload.wikimedia.org/wikipedia/commons/5/55/SFA_Polygon_with_hole.svg) |  [[[X1, Y1], [X2, Y2][ Xn, Yn]..[__X1__,__Y1__]],[[X1, Y1], [X2, Y2][ Xn, Yn]..[__X1__,__Y1__]]],  | [Relation](http://wiki.openstreetmap.org/wiki/Relation) |

> ##### Exercise 9
We have a point representing our holiday location. We have a line representing the flight route for an airplane. We have a polygon representing a country at war.The line crosses the polygon. What should we do?


### Multigeometries
You now know the basics of geometric primitives. Primitives are constructed from other primitives. As geometry is a mathematics branch, we can do all sort of operations with primitives that create other primitives. These are called advanced or multigeometry. In OpenStreetMap all of these advanced forms are stored in the database by using _relations_

| Type |  | Openstreetmap |
| -- | -- | -- |
| MultiPoint | ![](https://upload.wikimedia.org/wikipedia/commons/d/d6/SFA_MultiPoint.svg) |  [Relation](http://wiki.openstreetmap.org/wiki/Relation) |
| MultiLineString | ![](https://upload.wikimedia.org/wikipedia/commons/8/86/SFA_MultiLineString.svg) |  [Relation](http://wiki.openstreetmap.org/wiki/Relation) |
| MultiPolygon | ![](https://upload.wikimedia.org/wikipedia/commons/d/dc/SFA_MultiPolygon.svg) |  [Relation](http://wiki.openstreetmap.org/wiki/Relation) |
| MultiPolygon with holes| ![](https://upload.wikimedia.org/wikipedia/commons/3/3b/SFA_MultiPolygon_with_hole.svg) |  [Relation](http://wiki.openstreetmap.org/wiki/Relation) |

As you can see, these multigeometries are _collections_ of primitives. 

> ##### Exercise 10
Can you think of some real world example for the advanced primitives? Lets go through them.

We have learned about geometries, but how does this relate to maps? Think of a map as a way to _draw_ geometries. We have also learned about models. You should now be aware of the possibility to turn a geometry into a (part of a) model. So let us look at a map.

![](https://upload.wikimedia.org/wikipedia/commons/a/a1/Kirov_street%2C_Yaroslavl%2C_openstreetmap.PNG)


> ##### Exercise 11
- Can you distinguish geometry on the map?
- What models do you see?
- What other enhancements are made to make the map "readable"?



As you can see, almost all the geometries are on the map. Some are displayed as text. Others are enhanced by adding a width, color or symbol. There is only on thing that is hard to determine from this map. What is that?

You cannot tell __where on earth__ the map is.

## A place on earth

So how do we make maps and how do we make sure everybody can use them?  Mapmakers over the ages have made agreements on that.

### History

One of the oldest maps we know was created in the time of the [Babylonians](https://en.wikipedia.org/wiki/Early_world_maps#Babylonian_Imago_Mundi_.28c._600_BCE.29). You can see that it had no color. It needed a lot of text to explain the content of the map.

 ![](https://upload.wikimedia.org/wikipedia/commons/a/a5/Baylonianmaps.JPG)

In early history, the world was unknown to the mapmakers. The maps only described the _"known world"_.

![](https://upload.wikimedia.org/wikipedia/commons/a/a0/Anaximander_world_map-en.svg)
The world was seen as flat. Most of us now know that is not. Years of study has made people model the earth into a sphere. But again, that is a model. And different purposes require different models.

### Geodetic System

[Geodesy](https://en.wikipedia.org/wiki/Geodesy) is the scientific discipline that deals with the measurement and representation (model) of the earth. Geodetic engineers have created a standard called [World Geodetic System](https://en.wikipedia.org/wiki/World_Geodetic_System) that is a spheroidal reference surface that tries to be as close as possible to the nominal sealevel, everywhere on earth. This standard was created in 1984 and is often called __WGS84__. WGS84 is the standard coordinate system used by [GPS]() to register coordinates on, in and above the earth surface.

With this standard, we can model the earth as a sphere that can be used to collect coordinates, create models from these coordinates and create maps!

### Map Projection
You know how to peel an orange. But have you ever tried to flatten it?

![](https://www.learner.org/courses/mathilluminated/images/units/8/1819.png)

It is mathematically impossible to project a sphere on a plane without making concessions. This is a problem for map making. And that is why there are different methods for different purposes. And they all come with one or more caveats. The process of projecting our earth on a plane is possible by using projections. The wikipedia page on [map projections](https://en.wikipedia.org/wiki/Map_projection) explains this in detail.

There is a lot of computer software available to go from WGS84 coordinates to any possible map projection.

Combining coordinates that are registered in standard (WGS84) coordinates with a map projection allows computers to create maps that can be displayed on a plane (a piece of paper or a computer screen)

### Gathering coordinates

[Surveying](https://en.wikipedia.org/wiki/Surveying) is the technique, profession, and science of determining the terrestrial or three-dimensional position of points and the distances and angles between them. Surveying is all about gathering coordinates.

Surveying has always been of importance and went hand in hand with land ownership. Knowing the exact dimensions of a plot of land, means tax income. A good land registration prevents disputes. Surveyors have been with us since the ages of the Egyptians.

![](http://www.stalbertgazette.com/apps/pbcsi.dll/bilde?Site=GR&Date=20120623&Category=SAG0801&ArtNo=306239982&Ref=EP&NewTbl=1&item=2)

At first surveyors used ropes. Mainly to determine distances. Using mathematics to combine distances, they could calculate a surface area.

![](http://holmansnv.com/wp-content/uploads/2012/03/groma.jpg)

They created fantastic instruments.

![](https://upload.wikimedia.org/wikipedia/commons/b/b2/Bundesarchiv_Bild_183-S12054%2C_Vermessungstruppe_bei_Fernaufnahmen.jpg)

And people found employment in surveying.

![](https://upload.wikimedia.org/wikipedia/commons/f/f3/All_female_survey_crew_-_Minidoka_Project,_Idaho_1918.jpg)

Equipment modernized.

![](https://upload.wikimedia.org/wikipedia/commons/1/1a/Tide_station_leveling.jpg)

Evolved into GPS,

![](https://upload.wikimedia.org/wikipedia/commons/8/80/Field-Map_birdie.jpg)

And eventually, ended up in our smartphones.


![](https://upload.wikimedia.org/wikipedia/commons/0/0a/GPS_on_smartphone_cycling.JPG)

All you need to gather coordinates is a smartphone. Of course there are cases where the accuracy will not do, still requiring more advanced equipment or techniques. But a smartphone that records your trip as you walk or drive is a perfect start.


### Let's start mapping

We now have the knowledge required to start mapping. 
 - We know how to gather coordinates to model objects we observe
 - Draw the models
 - Connect lines, add width, color, text and texture to create a map.

> ##### Exercise 12
Below you find an image of random coordinates. Print the image and let the attendees draw a map. Let the attendees show the map and discuss it.

![](http://i.stack.imgur.com/2FdrL.png)


Recorded coordinates are not all we need. Context is important. We can provide context by taking pictures, memorizing and taking notes.

You are now ready to go on a field day. Make sure you are [prepared](preparation_fieldday.md). 









