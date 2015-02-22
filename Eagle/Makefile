
TARGETS=Picker.lbr
default: $(TARGETS)

Picker.lbr: PickerBase.lbr
	buildResolverParts.py --lbr $< --out $@

clean:
	rm -rf $(TARGETS)
