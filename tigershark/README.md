
## Tigershark

This folder is copied over from tigershark repository (https://github.com/sbuss/TigerShark) and is not following any
pre-commit rules.

Tigershark is used to parse x12 271 responses. It uses pyx12 maps under the hood, which have to be converted into
tigershark's python classes. The pyx12 map we use for the 271 response is the file `271.5010.X092.A1.xml`, and it
contains the structure of a 271 file.
In order to map this configuration file to a python class file, we have to run the following tigershark command:
- `python tools/convertPyX12.py ../../../map/271.5010.X092.A1.xml parsers/P271_5010_X092_A1.py -b pyx12/pyx12/map/ -n parsed_271`

> run this inside `home-app/tigershark/`

Running this code will generate a `P271_5010_X092_A1.py` file under `home-app/tigershark/parsers/`.

### Requirements
In order to run the convert command, please checkout the pyx12 repo inside tigershark folder:
- `https://github.com/azoner/pyx12.git`
