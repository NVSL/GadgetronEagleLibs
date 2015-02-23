 
TARGETS=KoalaBuild.lbr KoalaDesign.lbr
default: $(TARGETS)

KoalaBuild.lbr KoalaDesign.lbr: KoalaBase.lbr
	buildKoalaParts.py --baselib KoalaBase.lbr  --buildlib KoalaBuild.lbr --designlib KoalaDesign.lbr

clean:
	rm -rf $(TARGETS)
