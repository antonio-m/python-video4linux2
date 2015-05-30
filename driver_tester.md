# Introduction #

Simple program that test various functionality of a driver.
http://linuxtv.org/v4lwiki/index.php/Test_Suite#Test_applications

# Details #

I am not a v4l expert, but this needs to be written so I am giving it a shot.

call vidioc\_querycap and get a list of what else it exposes.  call them and make sure
things don't error.  call everything else and make sure it does error.  iterate though permutations, and or check edge conditions.

There is a test driver to the test against:
http://v4l.videotechnology.com/vivi.html
It is part of the standard kernel.