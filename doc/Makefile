# Copyright (c) 2011-2013, Universite de Versailles St-Quentin-en-Yvelines
#
# This file is part of ASK.  ASK is free software: you can redistribute
# it and/or modify it under the terms of the GNU General Public
# License as published by the Free Software Foundation, version 2.
#
# This program is distributed in the hope that it will be useful, but WITHOUT
# ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS
# FOR A PARTICULAR PURPOSE.  See the GNU General Public License for more
# details.
#
# You should have received a copy of the GNU General Public License along with
# this program; if not, write to the Free Software Foundation, Inc., 51
# Franklin Street, Fifth Floor, Boston, MA 02110-1301 USA.

VERSION := $(shell cat ../VERSION)
TARGET := ask-manual-$(VERSION).pdf

all: $(TARGET)

$(TARGET): ask-manual.tex
	pdflatex -shell-escape ask-manual.tex 
	mv ask-manual.pdf $(TARGET)

wiki:
	./latex2wiki/transform.sh

clean:
	rm -rf $(TARGET) *.log *.out *.toc *.aux build/ adaptive-sampling-kit.wiki/

.PHONY: wiki
