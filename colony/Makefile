# This will regenerate png files from ase (Aseprite) files
# by exporting individual layers to png.

all: houses.png walls.png

.PHONY: all

# This Makefile.
Makefile := $(lastword $(MAKEFILE_LIST))

# Run aseprite without starting the UI.
aseprite-cmd := aseprite --batch

houses.png: structure.ase $(Makefile)
	$(aseprite-cmd) --layer=houses structure.ase --save-as=$@

walls.png: structure.ase $(Makefile)
	$(aseprite-cmd) --layer=walls structure.ase --save-as=$@