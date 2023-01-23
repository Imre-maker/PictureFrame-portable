# PictureFrame-portable
At starting of the executable object I get Errors:FileNotFoundError: [Errno 2] No such file or directory: '/tmp/_MEI8C34IS/pi3d/shaders/std_head_vs.inc'

I had the target to make a version of PictureFrame2020.py that has mirror/monitor rotation functionality in order to see a portrait oriented picture as big as the landscape ones and with the same resolution (just like at projecting slides with a slide-projector). So with the aid of a raspi a rotatable monitor and a stepper motor the program can rotate the monitor 90° right to see your portrait picture on the full screen and at landscape pictures naturally back with -90°. If you use a beamer instead of a monitor you need onely a mirror-system in front of the beamer to be rotated. 
As I succeded to modify the PictureFrame.py I wanted to make a portable version of it, so that my friends, without spyder3 and python knowledges can use it too. Unfortunately the executable (Pyinstaller) PictureFrame object delivers Errors like these:

WARNING:pi3d.Display:create Display with (...use_glx=True) for transparent background on x11 window. libGLX needs to be available
Traceback (most recent call last):
  File "pi3d/Shader.py", line 192, in _load_shader
  File "pkg_resources/__init__.py", line 1167, in resource_string
  File "pkg_resources/__init__.py", line 1412, in get_resource_string
  File "pkg_resources/__init__.py", line 1579, in _get
  File "PyInstaller/loader/pyimod02_importers.py", line 344, in get_data
FileNotFoundError: [Errno 2] No such file or directory: '/tmp/_MEI8C34IS/pi3d/shaders/std_head_vs.inc'

During handling of the above exception, another exception occurred:

Traceback (most recent call last):
  File "PictureFrame_2MI_My.py", line 1194, in <module>
  File "pi3d/Shader.py", line 149, in create
  File "pi3d/Shader.py", line 110, in __init__
  File "pi3d/Shader.py", line 97, in make_shader
  File "pi3d/Shader.py", line 199, in _load_shader
  File "pi3d/Shader.py", line 195, in _load_shader
FileNotFoundError: [Errno 2] No such file or directory: 'std_head_vs.inc'
[2394] Failed to execute script 'PictureFrame_2MI_My' due to unhandled exception!

I wood be very thankfull if somebody could help me
