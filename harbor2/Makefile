# This will regenerate png files from ase (Aseprite) files
# by exporting individual layers to png.

land-layers  := dirt shadows

land-outputs := $(foreach l,$(land-layers),land-$(l).png)

all: $(land-outputs)

.PHONY: all

# This Makefile.
Makefile := $(lastword $(MAKEFILE_LIST))

# Run aseprite without starting the UI.
aseprite-cmd := aseprite --batch

land-%.png: land.ase
	$(aseprite-cmd) --layer=$* $^ --save-as=$@