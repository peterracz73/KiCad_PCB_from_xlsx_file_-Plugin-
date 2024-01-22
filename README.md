# KiCad PCB from xlsx file (Plugin)
                                                                              

Project for **[KiCad](https://www.kicad.org/)** action plugins with **[openpyxl](https://pypi.org/project/openpyxl/)**

**Table of Contents**

- [Key Features](#key-features)
- [How to use](#how-to-use)
  - [Install plugin](#install-plugin)
  - [Usage information](#Usage-information)
  - [Example xlsx file](#Example-xlsx-file)
- [License](#license)

## Key Features

- KiCad compatible plugin packaging
- Custom [repository](https://github.com/peterracz73/KiCad_PCB_from_xlsx_file_-Plugin-) installations for development builds
- Create PCB design
- Information from xlsx file
- Example xlsx file

## How to use

This is a project for the easy to make a PCB design from a xlsx file. The file includes all information from the PCB. Included the electrical parts, measure points, other information, and the all connections of the part's pins.

### Install plugin

The KiCad program is based on the Python programming language, so the language of this extension is also Python. You need some packages to run the program. Need the PIP and the openpyxl packages.

Use the command terminal.

First task install the PIP on the Python:

Version one:
```shell
python get-pip.py
```

Version two:
```shell
curl https://bootstrap.pypa.io/get-pip.py -o get-pip.py
```

The second task install the opensyxl package:

```shell
python -m pip install openpyxl
```

If the python or pip commands run to error, you need to include their paths of commands to the computer paths.  For example [this](https://www.computerhope.com/issues/ch000549.htm).

If the two packages were installed, you close the terminal windows and open the KiCad program.  After the program is running select the Plugin and Content Manager, then a window pops up. Here push the Install from File... button. Please browse and load the downloaded zip file, then the KiCad program installs the plugin.


### Usage information

First, create a new project and open the PCB. Now you have a blank PCB. Open the plugin with the icon from then menu bar:

![icon-and-gui-window](icon.png)

Then the plugin opened a window, where you can browse the source xlsx file. If you selected the file and wrote the offset values, you can start the process with the "Start process" button.

After the plugin was running, the KiCad show the components and networks on the PCB.

The plugin can insert shapes:
- offset cordinates
- measure points (Spear, Flat, Crown)
- electrical parts
- corner points
- pins of parts
- text

The example file includes example from shapes and syntaxis.



## Example xlsx file

The example file includes example from shapes and syntaxis.

[Download file](https://github.com/peterracz73/KiCad_PCB_from_xlsx_file_-Plugin-/raw/main/BoardSource.xlsx)


Columns mean in the file:

Offset coordinates:
- Pad instance: name of coordinate
- Net Name: not used
- Side: not used
- Head Type: type of cordinate (OffsetX or OffsetY)
- Probe Size: value of coordinate offset
- Fixture Location: not used
- sch: not used
- footprint: not used

Measure points (Spear, Flat, Crown)
- Pad instance: name of measure point
- Net Name: network name of measure point
- Side: indicative side of measure point
- Head Type: type of measure point (Spear, Crown, Flat)
- Probe Size:  indicative size of measure point
- Fixture Location: point locations (X mm*1000, Y mm-1000)
- sch: not used
- footprint: footprint file name and location on the computer (need full route)

Electrical parts
- Pad instance: name of part
- Net Name:  not used
- Side: indicative side of part
- Head Type: Part
- Probe Size:  rotate position of part
- Fixture Location: locations of part (X mm*1000, Y mm-1000)
- sch: not used
- footprint: footprint file name and location on the computer (need full route)

Corner points
- Pad instance: name of corner
- Net Name:  not used
- Side:  not used
- Head Type: type of corner (Corner1, Corner2)
- Probe Size:  thickness of corner line
- Fixture Location: locations of corner point (X mm*1000, Y mm-1000)
- sch: not used
- footprint: not used

Hole
- Pad instance: name of hole
- Net Name:  not used
- Side:  indicative side of hole
- Head Type: Hole
- Probe Size:  indicative side of hole
- Fixture Location: location of corner point (X mm*1000, Y mm-1000)
- sch: not used
- footprint:  footprint file name and location on the computer (need full route)

Pins of parts
- Pad instance: name of pin
- Net Name: name of measure point or network for pin
- Side:  indicative side of pin
- Head Type: Pin
- Probe Size:  Pin number
- Fixture Location:  not used
- sch: not used
- footprint:   not used

Text
- Pad instance: content of text
- Net Name: size of text
- Side:  indicative side of pin
- Head Type: Text
- Probe Size:  rotate position of text
- Fixture Location:  location of text  (X mm*1000, Y mm-1000)
- sch: not used
- footprint:   not used

Fixture Location types:

Fixture location has two types, relative and absolute:
- The absolute coordinate signal is a(.., ..). The plugin uses the PCB coordinate. 
- The relative coordinate signal is (.., ..). When used then relative coordinate the plugin modifies the coordinates with Offset.


## License

This project is distributed under the terms of the [MIT](https://github.com/peterracz73/KiCad_PCB_from_xlsx_file_-Plugin-/blob/main/LICENSE) license.
