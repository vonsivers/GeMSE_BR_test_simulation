# $Id: GNUmakefile,v 1.2 2003/01/23 15:31:39 maire Exp $
# --------------------------------------------------------------
# GNUmakefile for examples module.  Gabriele Cosmo, 06/04/98.
# --------------------------------------------------------------

name := GeMSE_BR_test
G4TARGET := $(name)
G4EXLIB := true

ROOTCFLAGS      = $(shell root-config --cflags)
ROOTLIBS        = $(shell root-config --libs)
ROOTGLIBS       = $(shell root-config --glibs)

EXTRALIBS +=$(ROOTLIBS)
EXTRALIBS +=$(ROOTGLIBS)

CPPFLAGS += $(ROOTCFLAGS)


ifndef G4INSTALL
  G4INSTALL = ../../..
endif

.PHONY: all
all: lib bin

include $(G4INSTALL)/config/binmake.gmk

visclean:
	rm -f g4*.prim g4*.eps g4*.wrl
	rm -f .DAWN_*
