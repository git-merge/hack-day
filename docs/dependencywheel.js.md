## DependencyWheel.js

Göran Bodenschlatz (coding46) and myself (Robert Reiz)(reiz) worked on dependency_wheel.js <https://github.com/versioneye/dependency_wheel>. This is JavaScript library to visualize connections between nodes. On <http://www.versioneye.com> it is used to visualize recursive dependencies of Software Libraries. Here is an example:

![](http://robertreiz.files.wordpress.com/2013/05/687474703a2f2f6d656469612d63616368652d6563352e70696e7465726573742e636f6d2f75706c6f61642f37323632303631323731313836373532325f475551696f6b76555f632e6a7067.jpeg "Dependency Wheel")

dependency_wheel.js is pure JavaScript. It uses a HTML 5 Canvas object to do the drawings.

At the GitMerge Hackathon we worked on it to display directions in the wheel. We did some brainstorming and came up with different solutions. At the end we decided to use different color for incoming and outgoing connections. Outgoing connections we marked now blue and incoming gree. Here is an image how it looks now with the hover effect.

![](http://robertreiz.files.wordpress.com/2013/05/screen-shot-2013-05-15-at-11-08-16-am.png "Dependency Wheel")

Here is another blog post about this work: <http://robert-reiz.com/2013/05/15/improving-the-dependency-wheel-at-the-gitmerge-hackathon/>.

We plan to use dependency_wheel.js for the <http://trophicgraph.com/> project to visualise foot chains.
