# cnc_tools
CNC-related programs

A set of Python programs and shell scripts to generate or modify data for different CNC tasks. Each Python program can be run as executable, provided the python interpreter is in /usr/bin/python. Alternatively, use python <program> <parameters> to run each tool. All Python programs support --help option to get usage.

Python programs:
- cylinder: make a gcode file that will mill a cylinder
- rectangle: make a gcode file that will mill a rectangle
- nc2gcode: convert a gcode file (<file>.nc) produced by MakerCAM to gcode suitable for a Marlin controller. Milling is distinguished from repositioning, so repositioning movements can be faster. All commands are converted to relative positioning. Starting position is assumed at the material surface. At the end, the tool is returned to the starting position.
- pcbsvg: Works on SVG files produced by Fritzing. Used in conjunction with Inkscape, it allows changing radius of selected circles and line widths of selected lines without altering their positions.

Shell scripts:
- ncg2gcode: converts gcode produced by Inkscape (usually <file>.ngc) to a form suitable for a Marlin controller.
