---
content_type: page
description: ''
learning_resource_types:
- Assignments
ocw_type: CourseSection
parent_title: Assignments
parent_type: CourseSection
parent_uid: c52938fb-f763-7324-f6dc-7edf3a9f1bd1
title: 'CsoundXO: Download and Instructions'
uid: 580501e1-fcb3-5707-178d-e2ac73d47b85
video_files:
  video_thumbnail_file: null
video_metadata:
  youtube_id: null
---

These instructions are provided by Wu-Hsi Li. (Courtesy of Wu-Hsi Li. Used with permission.)

Description
-----------

CsoundXO server, CsoundXO Python API, sample sounds, sample Python programs.

Software Download
-----------------

CsoundXO software package, by Barry Vercoe: ({{% resource_link 49d393b9-28aa-936e-b8f3-c00a692bb9bc "TAR - 37.2 MB" %}})

I wouldn't suggest you to download the file through Browse activity since the file management in XO is kind of tricky, but if you're interested, see [http://wiki.laptop.org/go/Journal\_Activity](http://wiki.laptop.org/go/Journal_Activity). Please download csoundxo.tar and Musicpainter.tar from your own computer, and copy to a flash disc.

Installation
------------

1.  plug your flash disc on XO, then open a terminal activity on XO
2.  "su" - become root
3.  "mount" - check the id of your flash disc
4.  "mount /dev/sda1 /mnt" - the device name varies, replace the device name with the actual one
5.  "exit" - exit root mode
6.  "cp /mnt/csoundxo.tar /home/olpc/csoundxo.tar"
7.  "cp /mnt/Musicpainter.tar /home/olpc/Activities/Musicpainter.tar"
8.  "tar -xvf csoundxo.tar"
9.  "su" - become root again
10.  "umount /mnt" - unmount
11.  "exit"

Music Demo 1
------------

A Whitney Houston piece:

1.  Python csndxogui.py
2.  press "launch server"
3.  press "connect" to localhost
4.  press "play 10whit"
5.  press "stop", and "disconnect", and "shutdown"

Music Demo 2
------------

Make two XOs play together on remote machine

1.  get a remote machine
2.  make sure both XOs connect to Internet or to the same mesh
3.  check the IP from the remote machine by "ifconfig" in the terminal
4.  go to the csoundxo folder, run csoundxo (./csoundxo)

On main machine

1.  Python csndxogui.py, press "launch server"
2.  enter the remote IP, press enter
3.  connect to both csound servers, make sure you see green lights on both sides
4.  press "duo performance"
5.  to stop, press "stop", "disconnect", "shutdown"