# Gamemaker frustum AABB intersection
This is a simple frustum AABB intersection check, useful for view culling.  
![alt text](https://github.com/callmeEthan/Gamemaker_frustum_culling/blob/main/Readme/clip.gif?raw=true)

## Usage
First supply the **view projection matrix** to get view planes
```
var view = matrix_get(matrix_view);
var proj = matrix_get(matrix_projection);
var matrix = matrix_multiply(view, proj);
frustum_setPlanes(matrix);
```
Then you can simply call frustum_intersectsBox and frustum_intersectsSphere to check for intersection
```
frustum_intersectsBox(xmin, ymin, zmin, xmax, ymax, zmax);
frustum_intersectsSphere(x, y, z, radius);
```
These function will returns **true** if object is within view, **false** otherwise.
