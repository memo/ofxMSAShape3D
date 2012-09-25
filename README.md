ofxMSAShape3D
=====================================

Introduction
------------
C++ openFrameworks addon wrapper for Vertex Arrays & Vertex Buffer Objects (coming soon) to allow Immediate mode style syntax on embedded systems / iPhone etc. (Probably now is superseded by built in ofMesh and ofVboMesh classes). 
Demo at [www.memo.tv/msashape3d](http://www.memo.tv/msashape3d).


Licence
-------
The code in this repository is available under the [MIT License](https://secure.wikimedia.org/wikipedia/en/wiki/Mit_license).  
Copyright (c) 2008-2012 Memo Akten, [www.memo.tv](http://www.memo.tv)  
The Mega Super Awesome Visuals Company


Installation
------------
Copy to your openFrameworks/addons folder.

Dependencies
------------
none

Compatibility
------------
openFrameworks 0072  
I am generally testing only with [openFrameworks](www.openframeworks.cc), however it should work with [Cinder](www.libcinder.org) too. If it doesn't, please file an issue.


Known issues
------------
none

Version history
------------
### v1.1    23/09/2012
- compatible with OF0072
- renamed (uppercase) MSA namespace to (lowercase) msa. (kept MSA as an alias for backwards compatibility)

### v1.0
- move to centralized MSALibs
- everything is msa:: namespace
- seperated interface and implementation in header file

### v0.8	16/05/2009
- fixed bug with normals and texture coordinates (thanks jonbro)

### v0.71	29/04/2009
- restores all client states to how they were before modding (only in safe mode)

### v0.6	07/04/2009
- changed license to revised BSD (a lot more more permissive than GPL)

### v0.5	 19/02/09
- renamed methods to avoid confusion with opengl functions:
   - glVertex is now addVertex
   - glColor is now setColor
   - glNormal is now setNormal
   - glTexCoord is now setTexCoord
   - glBegin / glEnd are now begin / end
   - glRect is now drawRect

- added safeMode option (on by default)
- with safeMode on (default):
   - array is automatically reallocated when space runs out
   - all client states are enabled and disabled as nessecary
- with safeMode off (for advanced users) you can get much better performance if you know what to do, see docs. 
- lots of other optimizations and restructuring
- all methods now inline
- using normal arrays instead of vectors

### v0.3	04/02/09
- added draw() to redraw the cached shape

### v0.2	30/01/09
- added glRect()

### v0.1	27/01/09
- initial version
