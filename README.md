rle-repair
==========

Volume repair and validation for narrow band level sets.  This is mainly used internally, but can also be useful for doing certain volume processing operations if you know what you are doing.  The main purpose of this code is to take as input disorganized collections of boundary points and then convert them into valid narrow band representations.

Installation
============
NPM:

    npm install rle-repair

Usage
=====
You can import the repair module like so:

    var repair = require("rle-repair");

All the repair methods work on VolumeBuilder objects.  If you give them a regular volume, they will fail.

`repair.resort(volume)`
-----------------------
Rearranges the runs of `volume` so that they are in proper sorted order.  This is done in place.

`repair.resurface(volume)`
--------------------------
Adds any missing surface runs to the volume.

`repair.removeDuplicates(volume)`
---------------------------------
Removes extra/redundant voxels.  This can also be used to trivially convert a voxel array into an rle volume, but it is not recommended.

`repair.fullRepair(volume)`
---------------------------
Calls all of the above methods in sequence.


Credits
=======
(c) 2013 Mikola Lysenko