---
content_type: page
description: ''
learning_resource_types:
- Assignments
ocw_type: CourseSection
parent_title: Assignments
parent_type: CourseSection
parent_uid: c52938fb-f763-7324-f6dc-7edf3a9f1bd1
title: 'Exercise 5: gtk + csoundxo'
uid: 93f0a1b5-afab-021e-f836-13fd5dc9817f
video_files:
  video_thumbnail_file: null
video_metadata:
  youtube_id: null
---

This material is by Wu-Hsi Li. (Courtesy of Wu-Hsi Li. Used with permission.)

\# Start by downloading gtkexercise.py ({{% resource_link 38f632b3-8c79-d485-00fe-8d6f0081b6e1 "PY" %}})  
\# "cd /home/olpc/Activities/Musicpainter.activity"  
\# We're going to borrow the csound orchestra, sound samples and  
#     other python programs from Musicpainter, so please put gtkexercise.py  
#     under the same folder with Musicpainter.activity.   
\# "fget http://www.media.mit.edu/~wuhsi/csoundxo/gtkexercise.py"  
  
\# If fget doesn't work, make sure your green machine is connected to the Internet.  
\# When the machine is connected, the browser should allow you to browse any webpage.  
\# Also, if you open a terminal, you can get your IP by the command "ifconfig".  
\# If you don't have a Internet IP, your machine is not connected (yet).  
  
\# You can use text editor like vi to edit your py file ("vi gtkexercise.py")  
\# Please try to read the python program  
  
\# To run the program, do "python gtkexercise.py"  
\# This program will display the keyboard and mouse events it captures on the screen  
\# Press "Escape" key to leave the program  
  
\# In key\_press\_event(), you can find the following line   
        # self.sendCsoundEvt("write your own csound line event")  
  
\# You can try to rewrite the event string  
  
csound1.sendLinevt("i8 0 2 1 0")    
csound1.sendLinevt("i1 0 1 1 7.00")         # format information see below  
csound1.sendLinevt("i1 0 1 1 7.02")         # these are a note event with finite duration  
csound1.sendLinevt("i1 0 1 1 7.04")  
csound1.sendLinevt("i1 0 1 2 7.04")  
csound1.sendLinevt("i1 0 5 2 7.04")  
  
\# line event format  
#  
\# field 1: instrument, 1: piano, 2: accordion, 3: string, 4: pizz, 5: clarinet, 6: guitar, 7: bass, 8: percussion  
\# field 2: start time (sec)  
\# field 3: duration (sec)  
\# field 4: volume, 1.0 = normal  
\# field 5: for percussion instrument, assign 0 ~ 17 for different sounds  
#         for pitch instrument, assign a.bb,  
#         for example 8.00 is a C5, 8.01 is C#5, 8.02 is D5, 7.00 is a C4  
  
\# If you rewrite both event strings in key\_press\_event and key\_release\_event  
\# the duration of note\_on event should be assigned -1 (infinite)  
\# and the duration of note\_off event should be assigned 0