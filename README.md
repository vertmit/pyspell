<img src="https://raw.githubusercontent.com/vertmit/PolygonCollision/aa4848617edbad97b15d97c889084a235e973b6f/logo.png" width="200"/>
<br>

PolygonCollision is a Python module designed for efficient collision detection between 2D polygons. Using the Separating Axis Theorem (SAT), this library enables precise detection of intersections between polygons, making it an essential tool for game developers, simulations, and applications requiring accurate collision detection between shapes.

# Features:
Polygon Collision Detection: Determine whether two 2D polygons overlap with accurate collision detection algorithms.
Customizable Shapes: Define custom 2D shapes by specifying their vertices as Vector objects.
Calculate verlocity: Calculate the verlocity between two different shapes.
Efficient Algorithm: Implementing the Separating Axis Theorem (SAT) ensures fast and reliable collision detection for complex polygons.

# How It Works:
The library checks for collisions by projecting the shapes onto various axes and checking if the projections overlap. If there is no axis along which the projections of the two shapes do not overlap, they are colliding.

# Code Examples:
```Python
import PolygonCollision

#Create Squares
polygon1 = PolygonCollision.shape.Shape(vertices = [(0, 0), (0, 10), (10, 10), (10, 0)])
polygon2 = PolygonCollision.shape.Shape(vertices = [(5, 5), (5, 15), (15, 15), (15, 5)], fill=False)

#Create Circle
circle = PolygonCollision.shape.Shape(vertices = [(30, 30)], radius = 5)

#Output The Size And Posiotion Of The Shapes
print('polygon1:', polygon1.get_width(), polygon1.get_height())

#Check For Polygons Collision
if polygon1.collide(polygon2):
    print('POLYGON COLLISION!!!')
else:
    print('no polygon colllision')

#Check For Polygons + Circle Collision
if polygon1.collide(polygon2):
    print('CIRCLE COLLISION!!!')
else:
    print('no circle colllision')
```
Output
```Output
POLYGON COLLISION!!!
no circle collision
```
# License:
This Collision Detection Library is licensed under the MIT License - see the LICENSE file for details.