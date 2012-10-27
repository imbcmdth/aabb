# AABB

_Axis-Aligned Bounding Boxes_

## Introduction

## Installation

````
npm install aabb
````

## Usage

## Examples

TODO

## APIs

### AABB

#### <span class="heading">constructor</span> `(min = [0,0,0], max = [0,0,0])`

`min` the minimum coordinates of the AABB. In a 2-D AABB in screen space, the coordinates for the upper-left corner.

`max` the maximum coordinates of the AABB. In a 2-D AABB in screen space, the coordinates for the lower-right corner.

Constructs a new AABB of dimensionality equal to `min.length` using the specified bounds.

*NOTE* The number of elements in `min` and `max` (ie. the dimensions) must be the same.

#### <span class="heading">getLength</span> `(axis)`

`axis` the zero-based array index representing a particular axis. By convention, 0 = x, 1 = y, 2 = z, and so on.

Returns the length of the AABB along the side defined by `axis`.

#### <span class="heading">getLengths</span> `()`

Returns an array containing the lengths of all sides of the AABB.

#### <span class="heading">expandByAABB</span> `(otherAABB)`

Expand `this` to contain `otherAABB`.

#### <span class="heading">expandToContainElements</span> `(elements, startAt = 0)`

`elements` an array of elements.

`startAt` offset into the `elments` which to start at.

Expand `this` to contain all `elements`.

#### <span class="heading">makeToContainElements</span> `(elements)`

`elements` an array of elements.

Return a new AABB that contains the bounds of all `elements`.

#### <span class="heading">overlaps</span> `(otherAABB)`

Returns `true` if `this` and `otherAABB` overlap each other.

#### <span class="heading">contains</span> `(otherAABB)`

Returns `true` if `this` completely contains `otherAABB`.

#### <span class="heading">contained</span> `(otherAABB)`

Returns `true` if `this` is completely contained by `otherAABB`.

#### <span class="heading">getSurfaceArea</span> `()`

Returns the surface area of the AABB. In the 2 dimension case, this is the AABB's perimeter.

#### <span class="heading">getVolume</span> `()`

Returns the volume of the AABB. In the 2 dimension case, this is the AABB's area.

#### <span class="heading">clone</span> `()`

Returns a clone of `this`.

#### <span class="heading">intersectWithRay</span> `(ray)`

`ray` a ray to test against.

Returns `false` is no intersection is possible. Otherwise, returns the portion of the ray (a ray segment) that results from the intersection of the ray with the AABB.

#### <span class="heading">intersectWithSegment</span> `(rs)`

`rs` - a ray segment to test against.

Returns `false` is no intersection is possible. Otherwise, returns the portion of the ray segment that results from the intersection of the ray segment with the AABB.