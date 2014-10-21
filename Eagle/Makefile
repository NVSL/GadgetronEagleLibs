
TARGETS=Resistors.lbr Capacitors.lbr
default: $(TARGETS)

%.lbr: %.devspec %.base.lbr
	devFamily.py --db $< --lbrin $*.base.lbr --lbrout $@

clean:
	rm -rf $(TARGETS)