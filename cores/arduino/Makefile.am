AM_CFLAGS = -c -g -Os -ffunction-sections -fdata-sections -MMD -flto -fno-fat-lto-objects
AM_CXXFLAGS = -c -g -Os -fpermissive -fno-exceptions -ffunction-sections -fdata-sections -fno-threadsafe-statics -Wno-error=narrowing -MMD -flto
ARFLAGS = rcs
AM_LDFLAGS =

lib_LIBRARIES = \
    libcore-uno.a \
    libcore-mega2560.a \
    libcore-micro.a \
    libcore-nano.atmega328.a

include_HEADERS = \
    Arduino.h \
    Client.h \
    HardwareSerial.h \
    HardwareSerial_private.h \
    IPAddress.h \
    PluggableUSB.h \
    Print.h \
    Printable.h \
    Server.h \
    Stream.h \
    USBAPI.h \
    USBCore.h \
    USBDesc.h \
    Udp.h \
    WCharacter.h \
    WString.h \
    binary.h \
    new \
    new.h \
    wiring_private.h

COMMON_SRCS = \
    CDC.cpp \
    HardwareSerial.cpp \
    HardwareSerial0.cpp \
    HardwareSerial1.cpp \
    HardwareSerial2.cpp \
    HardwareSerial3.cpp \
    IPAddress.cpp \
    PluggableUSB.cpp \
    Print.cpp \
    Stream.cpp \
    Tone.cpp \
    USBCore.cpp \
    WInterrupts.c \
    WMath.cpp \
    WString.cpp \
    abi.cpp \
    hooks.c \
    main.cpp \
    new.cpp \
    wiring.c \
    wiring_analog.c \
    wiring_digital.c \
    wiring_pulse.c \
    wiring_shift.c

libcore_uno_a_SOURCES = $(COMMON_SRCS)
libcore_uno_a_CPPFLAGS = \
    -mmcu=atmega328p \
    -DF_CPU=16000000L \
    -DARDUINO=@RUNTIME_IDE_VERSION@ \
    -DARDUINO_AVR_UNO \
    -DARDUINO_ARCH_AVR \
    -DVARIANT_STANDARD \
    -I$(srcdir)/../../variants/standard 

libcore_mega2560_a_SOURCES=$(COMMON_SRCS)
libcore_mega2560_a_CPPFLAGS=\
    -mmcu=atmega2560 \
    -DF_CPU=16000000L \
    -DARDUINO=@RUNTIME_IDE_VERSION@ \
    -DARDUINO_AVR_MEGA2560 \
    -DARDUINO_ARCH_AVR \
    -DVARIANT_MEGA \
    -I$(srcdir)/../../variants/mega 

libcore_micro_a_SOURCES = $(COMMON_SRCS)
libcore_micro_a_CPPFLAGS = \
    -mmcu=atmega32u4 \
    -DF_CPU=16000000L \
    -DARDUINO=@RUNTIME_IDE_VERSION@ \
    -DARDUINO_AVR_MICRO \
    -DARDUINO_ARCH_AVR \
    -DVARIANT_MICRO \
    -DUSB_VID=0x2341 -DUSB_PID=0x8037 "-DUSB_PRODUCT=\"Arduino Micro\"" \
    -I$(srcdir)/../../variants/micro 

libcore_nano_atmega328_a_SOURCES = $(COMMON_SRCS)
libcore_nano_atmega328_a_CPPFLAGS = \
    -mmcu=atmega328p \
    -DF_CPU=16000000L \
    -DARDUINO=@RUNTIME_IDE_VERSION@ \
    -DARDUINO_AVR_NANO \
    -DARDUINO_ARCH_AVR \
    -DVARIANT_EIGHTANALOGINPUTS \
    -I$(srcdir)/../../variants/eightanaloginputs 