# This will regenerate png files from ase (Aseprite) files
# by exporting individual layers to png.

land-layers   := dirt shadows
dock-layers   := overlay dock shadows
houses-layers := buildings smoke docks

land-outputs   := $(foreach l,$(land-layers),land-$(l).png)
dock-outputs   := $(foreach l,$(dock-layers),dock-$(l).png)
houses-outputs := $(foreach l,$(houses-layers),houses-$(l).png)

all: $(land-outputs) $(dock-outputs) $(houses-outputs)

.PHONY: all

# This Makefile.
Makefile := $(lastword $(MAKEFILE_LIST))

# Run aseprite without starting the UI.
aseprite-cmd := aseprite --batch

land-%.png: land.ase
	$(aseprite-cmd) --layer=$* $^ --save-as=$@

dock-%.png: dock.ase
	$(aseprite-cmd) --layer=$* $^ --save-as=$@

houses-%.png: houses.ase
	$(aseprite-cmd) --layer=$* $^ --save-as=$@