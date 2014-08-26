default: ../EAGLE/Artwork.lbr

LOGOS=$(wildcard *.png)

../EAGLE/Artwork.lbr : $(LOGOS) 
	for i in $(LOGOS); do pngToLine.py --png $$i --lbr $@ --force --width 0.025; done

clean: