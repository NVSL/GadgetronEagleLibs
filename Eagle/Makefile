CBC_LBR_TRANSLATOR := cbc_eagle_lbr_translator.py
IN_LBR = $(shell find . -name "*.lbr")
OUT_DIR := CbC_Library
OUT_PY = $(patsubst %.lbr, $(OUT_DIR)/%.py, $(IN_LBR))
 
TARGETS=KoalaBuild.lbr KoalaDesign.lbr $(OUT_PY)
default: $(TARGETS)

KoalaBuild.lbr KoalaDesign.lbr: KoalaBase.lbr
	buildKoalaParts.py --baselib KoalaBase.lbr  --buildlib KoalaBuild.lbr --designlib KoalaDesign.lbr

clean:
	rm -rf $(TARGETS)
	rm -rf $(OUT_DIR)

$(OUT_DIR)/%.py : %.lbr
	$(CBC_LBR_TRANSLATOR) -i $< -o $@

