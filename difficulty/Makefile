# Converts ase files into png (merging layers).

all: characters.png

.PHONY: all

# This Makefile.
Makefile := $(lastword $(MAKEFILE_LIST))

# Run aseprite without starting the UI.
aseprite-cmd := aseprite --batch

characters.png: characters.ase $(Makefile)
	$(aseprite-cmd) characters.ase --save-as=$@