SUBDIRS = cores/arduino libraries/EEPROM # libraries/HID libraries/SoftwareSerial libraries/SPI libraries/Wire
# dist_doc_DATA = README.md

AM_CFLAGS = -c -g -Os -ffunction-sections -fdata-sections -MMD -flto -fno-fat-lto-objects
AM_CXXFLAGS = -c -g -Os -fpermissive -fno-exceptions -ffunction-sections -fdata-sections -fno-threadsafe-statics -Wno-error=narrowing -MMD -flto
ARFLAGS = rcs
ELF2EEP = $(OBJCOPY) -O ihex -j .eeprom --set-section-flags=.eeprom=alloc,load --no-change-warnings --change-section-lma .eeprom=0
ELF2HEX = $(OBJCOPY) -O ihex -R .eeprom

include_HEADERS = variants/pins_arduino.h

nobase_include_HEADERS = \
    variants/circuitplay32u4/pins_arduino.h \
    variants/eightanaloginputs/pins_arduino.h \
    variants/ethernet/pins_arduino.h \
    variants/gemma/pins_arduino.h \
    variants/leonardo/pins_arduino.h \
    variants/mega/pins_arduino.h \
    variants/micro/pins_arduino.h \
    variants/robot_control/pins_arduino.h \
    variants/robot_motor/pins_arduino.h \
    variants/standard/pins_arduino.h \
    variants/yun/pins_arduino.h