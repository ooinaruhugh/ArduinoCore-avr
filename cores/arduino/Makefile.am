AM_CFLAGS = -shared -c -g -Os -ffunction-sections -fdata-sections -MMD -flto -fno-fat-lto-objects
AM_CXXFLAGS = -shared -c -g -Os -fpermissive -fno-exceptions -ffunction-sections -fdata-sections -fno-threadsafe-statics -Wno-error=narrowing -MMD -flto
ARFLAGS = rcs
AM_LDFLAGS = -shared

lib_LIBRARIES = \
    libcore-arduino-avr-uno.a \
    libcore-arduino-avr-mega2560.a

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

libcore_arduino_avr_uno_a_SOURCES = $(COMMON_SRCS)
libcore_arduino_avr_uno_a_CFLAGS= \
    $(AM_CFLAGS) \
    -mmcu=atmega328p \
    -DF_CPU=16000000L \
    -DARDUINO=10806 \
    -DARDUINO_AVR_UNO \
    -DARDUINO_ARCH_AVR \
    -I$(srcdir)/../../variants/standard 

libcore_arduino_avr_uno_a_CXXFLAGS= \
    $(AM_CXXFLAGS) \
    -mmcu=atmega328p \
    -DF_CPU=16000000L \
    -DARDUINO=10806 \
    -DARDUINO_AVR_UNO \
    -DARDUINO_ARCH_AVR \
    -I$(srcdir)/../../variants/standard

libcore_arduino_avr_mega2560_a_SOURCES = $(COMMON_SRCS)
libcore_arduino_avr_mega2560_a_CFLAGS= \
    $(AM_CFLAGS) \
    -mmcu=atmega2560 \
    -DF_CPU=16000000L \
    -DARDUINO=10806 \
    -DARDUINO_AVR_MEGA2560 \
    -DARDUINO_ARCH_AVR \
    -I$(srcdir)/../../variants/mega 

libcore_arduino_avr_mega2560_a_CXXFLAGS= \
    $(AM_CXXFLAGS) \
    -mmcu=atmega2560 \
    -DF_CPU=16000000L \
    -DARDUINO=10806 \
    -DARDUINO_AVR_MEGA2560\
    -DARDUINO_ARCH_AVR \
    -I$(srcdir)/../../variants/mega