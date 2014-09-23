---
layout: post
title: "[Mesh] Improving topology"
date: 2014-09-18 08:23:13 +0800
comments: true
categories: mesh, topology
---
Here I collect several ways for improving topology.

<!--More-->
##Edge Reduce

Merge the 2 end vertices of 2 red-edges

![](http://coding-addict.com/pictures/blender/edge-reduce-1.png)

![](http://coding-addict.com/pictures/blender/edge-reduce-2.png)

##Fill Pentagon Hole

![](http://coding-addict.com/pictures/blender/solve-pentagon-hole-pattern-1.png)

![](http://coding-addict.com/pictures/blender/solve-pentagon-hole-pattern-2.png)

![](http://coding-addict.com/pictures/blender/solve-pentagon-hole-pattern-3.png)

![](http://coding-addict.com/pictures/blender/solve-pentagon-hole-pattern-4.png)

![](http://coding-addict.com/pictures/blender/solve-pentagon-hole-pattern-5.png)

![](http://coding-addict.com/pictures/blender/solve-pentagon-hole-pattern-6.png)

##Redirect Topology

We want to make an new edge loop around eyes.

![](http://coding-addict.com/pictures/blender/redirect-topology-1.png)

Delete faces, then merge vertices.

![](http://coding-addict.com/pictures/blender/redirect-topology-2.png)

After that, the new edge loop has been made. Delete the faces we don't need.

![](http://coding-addict.com/pictures/blender/redirect-topology-3.png)


##Remove 5 edges vertex

![](http://coding-addict.com/pictures/blender/remove-penta-vertex-1.png)

![](http://coding-addict.com/pictures/blender/remove-penta-vertex-2.png)

![](http://coding-addict.com/pictures/blender/remove-penta-vertex-3.png)


Finally, we have eliminated one penta-edge vertex.
![](http://coding-addict.com/pictures/blender/remove-penta-vertex-4.png)