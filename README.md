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
```shell
python get-pip.py
```

The second task install the opensyxl package:

```shell
pip install openpyxl
```

If the python or pip commands run to error, you need to include their paths of commands to the computer paths.  For example [this](https://www.computerhope.com/issues/ch000549.htm).

If the two packages were installed, you close the terminal windows and open the KiCad program.  After the program is running select the Plugin and Content Manager, then a window pops up. Here push the Install from File... button.

Please browse and load the downloaded zip file, then the KiCad program installs the plugin.

