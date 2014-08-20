UTIL=../../Util/PCBArt/

default: ../PADS/Logos.l ../PADS/Squares.l

LOGOS=$(wildcard *Logo*.png)

SQUARES=$(wildcard *Square*.png)

../PADS/Logos.l : $(LOGOS:.png=.l) 
	$(UTIL)/lCat.py $^ >$@
	@ echo @@@@@@@@@@@@@@@@@@@  You still need to import the  @@@@@@@@@@@@@@@@@
	@ echo @@@@@@@@@@@@@@@@@@@   contents of $@ into $*.pt9   @@@@@@@@@@@@@@@@@

../PADS/Squares.l : $(SQUARES:.png=.l) 
	$(UTIL)/lCat.py $^ >$@
	@ echo @@@@@@@@@@@@@@@@@@@  You still need to import the  @@@@@@@@@@@@@@@@@
	@ echo @@@@@@@@@@@@@@@@@@@   contents of $@ into $*.pt9   @@@@@@@@@@@@@@@@@

%.l : %.png 
	$(UTIL)/pngToLine.py $< $@


clean:
	rm -rf *.l