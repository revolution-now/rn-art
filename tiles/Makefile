# This will regenerate png files from ase (Aseprite) files
# by exporting individual layers to png.

coast-layers  := beach border sand stencils surf
rivers-layers := bank cycle water

coast-outputs := $(foreach l,$(coast-layers),coast-$(l).png)
rivers-outputs := $(foreach l,$(rivers-layers),rivers-$(l).png)

all: $(coast-outputs) $(rivers-outputs) forest.png resources.png

.PHONY: all

# This Makefile.
Makefile := $(lastword $(MAKEFILE_LIST))

# Run aseprite without starting the UI.
aseprite-cmd := aseprite --batch

coast-%.png: coast.ase $(Makefile)
	$(aseprite-cmd) --layer=$* coast.ase --save-as=$@

rivers-%.png: rivers.ase $(Makefile)
	$(aseprite-cmd) --layer=$* rivers.ase --save-as=$@

forest.png: forest.ase
	$(aseprite-cmd) --all-layers forest.ase --save-as=$@

resources.png: resources.ase
	$(aseprite-cmd) --layer=icons resources.ase --save-as=$@