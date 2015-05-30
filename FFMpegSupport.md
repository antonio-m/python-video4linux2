# Introduction #

As the only library out there which interfaces Python and encoding videos is pymedia, I've begun interfacing pyv4l2 with libavcodec for native video capturing straight from the capture device. As such, you'll need to build the ffmpeg libraries with shared support so that pyv4l2 can take advantage of them through ctypes.

# Source Installation #

Switch to the directory that you keep all of your library sources in and type the following. Remove any libraries that you don't need from the ./configure line, but if you're like me and do a lot of video testing, I suggest that you keep them in.

```
git clone git://git.mplayerhq.hu/ffmpeg/
cd ffmpeg
git clone git://git.mplayerhq.hu/libswscale/
./configure --enable-shared --enable-gpl --enable-postproc--enable-swscale --enable-avfilter --enable-avfilter-lavf --enable-pthreads --enable-libamr-nb --enable-libamr-wb --enable-libdirac --enable-libfaac --enable-libfaad --enable-libmp3lame --enable-libspeex --enable-libtheora --enable-libvorbis --enable-libx264
make
sudo make install
```

# Ubuntu Installation #

```
sudo apt-get install ffmpeg
```

# Gentoo Installation #

```
sudo emerge -av ffmpeg
```