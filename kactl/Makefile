LATEXCMD = pdflatex -shell-escape
export max_print_line = 1048576

.PHONY: help
help:
	@echo "This makefile builds KACTL"
	@echo ""
	@echo "Available commands are:"
	@echo "	make fast	- to build the KACTL, quickly (only runs LaTeX once)"
	@echo "	make kactl	- to build the KACTL"
	@echo "	make clean	- to clean up the build process"
.PHONY: fast
fast:
	cd build && $(LATEXCMD) kactl.tex </dev/null
	cp build/kactl.pdf kactl.pdf

.PHONY: kactl
kactl:
	cd build && $(LATEXCMD) kactl.tex && $(LATEXCMD) kactl.tex
	cp build/kactl.pdf kactl.pdf

.PHONY: clean
clean: 
	cd build && rm -f kactl.aux kactl.log kactl.tmp kactl.toc kactl.pdf kactl.ptc





