
TARGETS=PickerBuild.lbr PickerDesign.lbr
default: $(TARGETS)

PickerBuild.lbr PickerDesign.lbr: PickerBase.lbr
	buildResolverParts.py --baselib PickerBase.lbr  --buildlib PickerBuild.lbr --designlib PickerDesign.lbr

clean:
	rm -rf $(TARGETS)
