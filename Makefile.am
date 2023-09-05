SUBDIRS = cores/arduino # libraries/EEPROM libraries/HID libraries/SoftwareSerial libraries/SPI libraries/Wire
# dist_doc_DATA = README.md

AM_CFLAGS = -c -g -Os -ffunction-sections -fdata-sections -MMD -flto -fno-fat-lto-objects
AM_CXXFLAGS = -c -g -Os -fpermissive -fno-exceptions -ffunction-sections -fdata-sections -fno-threadsafe-statics -Wno-error=narrowing -MMD -flto
AM_ARFLAGS = rcs
OBJCOPY_EEP_FLAGS = -O ihex -j .eeprom --set-section-flags=.eeprom=alloc,load --no-change-warnings --change-section-lma .eeprom=0
ELF2HEX = $(OBJCOPY) -O ihex -R .eeprom