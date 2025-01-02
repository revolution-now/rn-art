# Converts ase files into png (merging layers).

all: discoverer.png

.PHONY: all

# This Makefile.
Makefile := $(lastword $(MAKEFILE_LIST))

# Run aseprite without starting the UI.
aseprite-cmd := aseprite --batch

%.png: %.ase $(Makefile)
	$(aseprite-cmd) $*.ase --save-as=$@