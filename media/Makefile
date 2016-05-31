TARGET=Textures.xbt

IMAGES := $(shell find . -name "*jpg")
IMAGES += $(shell find . -name "*png")
IMAGES += $(shell find . -name "*gif")

all: $(TARGET)

.PHONY: force

$(TARGET): $(IMAGES)
ifeq (arm,arm)
	/mnt/package/mediacenter-osmc/src/xbmc-c327c53ac5346f71219e8353fe046e43e4d4a827/tools/depends/native/TexturePacker/bin/TexturePacker -dupecheck -use_none -input . -output $(TARGET)
else
	/mnt/package/mediacenter-osmc/src/xbmc-c327c53ac5346f71219e8353fe046e43e4d4a827/tools/depends/native/TexturePacker/bin/TexturePacker -dupecheck -input . -output $(TARGET)

endif

clean:
	rm -f $(TARGET)
distclean: clean

