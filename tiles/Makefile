# This will regenerate png files from ase (Aseprite) files
# by exporting individual layers to png.

coast-layers := \
  stencils      \
	surf          \
	border        \
	beach

coast-outputs := $(foreach l,$(coast-layers),coast-$(l).png)

all: $(coast-outputs)

.PHONY: all

# This Makefile.
Makefile := $(lastword $(MAKEFILE_LIST))

coast-ase := coast.ase

# Run aseprite without starting the UI.
aseprite-cmd := aseprite --batch

coast-%.png: $(coast-ase) $(Makefile)
	$(aseprite-cmd) --layer=$* $(coast-ase) --save-as=$@