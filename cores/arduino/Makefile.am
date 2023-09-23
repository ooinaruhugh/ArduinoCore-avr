AM_CFLAGS = -c -g -Os -ffunction-sections -fdata-sections -MMD -flto -fno-fat-lto-objects
AM_CXXFLAGS = -c -g -Os -fpermissive -fno-exceptions -ffunction-sections -fdata-sections -fno-threadsafe-statics -Wno-error=narrowing -MMD -flto
ARFLAGS = rcs
AM_LDFLAGS =

lib_LIBRARIES = \
    libcore-uno.a \
    libcore-mega2560.a \
    libcore-micro.a

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
AVR_UNO_COMMON_FLAGS = \
    -mmcu=atmega328p \
    -DF_CPU=16000000L \
    -DARDUINO=@RUNTIME_IDE_VERSION@ \
    -DARDUINO_AVR_UNO \
    -DARDUINO_ARCH_AVR \
    -DVARIANT_STANDARD \
    -I$(srcdir)/../../variants/standard 

libcore_uno_a_CFLAGS= \
    $(AM_CFLAGS) \
    $(AVR_UNO_COMMON_FLAGS)

libcore_uno_a_CXXFLAGS= \
    $(AM_CXXFLAGS) \
    $(AVR_UNO_COMMON_FLAGS)

libcore_mega2560_a_SOURCES = $(COMMON_SRCS)
AVR_MEGA2560_COMMON_FLAGS= \
    -mmcu=atmega2560 \
    -DF_CPU=16000000L \
    -DARDUINO=@RUNTIME_IDE_VERSION@ \
    -DARDUINO_AVR_MEGA2560 \
    -DARDUINO_ARCH_AVR \
    -DVARIANT_MEGA \
    -I$(srcdir)/../../variants/mega 

libcore_mega2560_a_CFLAGS= \
    $(AM_CFLAGS) \
    $(AVR_MEGA2560_COMMON_FLAGS)

libcore_mega2560_a_CXXFLAGS= \
    $(AM_CXXFLAGS) \
    $(AVR_MEGA2560_COMMON_FLAGS)

libcore_micro_a_SOURCES = $(COMMON_SRCS)
AVR_MICRO_COMMON_FLAGS = \
    -mmcu=atmega32u4 \
    -DF_CPU=16000000L \
    -DARDUINO=@RUNTIME_IDE_VERSION@ \
    -DARDUINO_AVR_MICRO \
    -DARDUINO_ARCH_AVR \
    -DUSB_VID=0x2341 -DUSB_PID=0x8037 -DUSB_MANUFACTURER=Unknown "-DUSB_PRODUCT=\"Arduino Micro\"" \
    -I$(srcdir)/../../variants/micro 

libcore_micro_a_CFLAGS= \
    $(AM_CFLAGS) \
    $(AVR_MICRO_COMMON_FLAGS)

libcore_micro_a_CXXFLAGS= \
    $(AM_CXXFLAGS) \
    $(AVR_MICRO_COMMON_FLAGS)