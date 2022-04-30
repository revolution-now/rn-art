# This will regenerate png files from ase (Aseprite) files
# by exporting individual layers to png.

coast-layers := \
	beach         \
	border        \
	sand          \
  stencils      \
	surf

coast-outputs := $(foreach l,$(coast-layers),coast-$(l).png)

all: $(coast-outputs) forest.png

.PHONY: all

# This Makefile.
Makefile := $(lastword $(MAKEFILE_LIST))

coast-ase := coast.ase

# Run aseprite without starting the UI.
aseprite-cmd := aseprite --batch

coast-%.png: $(coast-ase) $(Makefile)
	$(aseprite-cmd) --layer=$* $(coast-ase) --save-as=$@

forest.png: forest.ase
	$(aseprite-cmd) --all-layers forest.ase --save-as=$@