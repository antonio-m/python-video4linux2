Summary says it all. I've been trying to find an existing project for python to video4linux2 coding, but no one else seems to have released any files to download yet, so here we are!

You'll need SVN in order to check out my current implementation. Documentation is not provided at this point, but the main file contains device information checks by running it (python pyv4l2.py), and check out the recordpics.py for a sample program to save JPEG images from a particular device and input such as

```
cd python-video4linux
make
./pyv4l2.py
./streampics.py /dev/video0 0 BGR3 640 480 testpics
```

The next things which I would like to do with the library is to add video saving support using libtheora. The latter will probably be its own extension named python-theora.

I definitely need help with distutils, internationalization, and performance patches if anyone would wish to help. The current version does about 27.5fps on my Happugage ImpactVCB test card with the mmap interface, which is almost that of the NTSC standard at 29.97 fps.

Note: JPEG saving functionality requires the python imaging library (emerge -av imaging for us Gentoo users 8-)