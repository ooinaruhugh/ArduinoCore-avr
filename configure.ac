AC_INIT([ArduinoCore-avr],[1.8.6],[kafe@kafe.dev])
AC_DEFINE([RUNTIME_IDE_VERSION],[10806],[
   the version number of the Arduino core as a number (this uses two digits per version number
   component, and removes the points and leading zeroes, so 1.8.6 becomes `01.08.06` which becomes
   `runtime.ide.version=10806`).
])

AC_CONFIG_SRCDIR([cores/arduino/Arduino.h])
AC_CONFIG_AUX_DIR([build-aux])

AM_INIT_AUTOMAKE([foreign no-exeext])
AM_SILENT_RULES([yes])

cross_compiling=yes
AC_PROG_MAKE_SET
AC_PROG_CC([avr-gcc])
AC_PROG_CXX([avr-g++])

# Checks for programs.

AC_CHECK_TOOL(AS, avr-as, avr-as)
AM_PROG_AS([avr-as])
AC_CHECK_TOOL(RANLIB, avr-gcc-ranlib, avr-ranlib)
AC_CHECK_TOOL(AR, avr-gcc-ar, avr-ar)
AC_CHECK_TOOL(OBJCOPY, avr-objcopy, avr-objcopy)
AC_CHECK_TOOL(SIZE, avr-size, avr-size)

# Make sure that we found the right avr cross-compiler.

case "${CC}" in
   *gcc*)
       case "X`${CC} -dumpmachine`X" in
           XavrX) ;;
           *) AC_MSG_ERROR(Wrong C compiler found; check the PATH!) ;;
       esac
       ;;
   *) AC_MSG_ERROR(Wrong C compiler found; check the PATH!) ;;
esac
case "${CXX}" in
   *g++*)
       case "X`${CXX} -dumpmachine`X" in
           XavrX) ;;
           *) AC_MSG_ERROR(Wrong C++ compiler found; check the PATH!) ;;
       esac
       ;;
   *) AC_MSG_ERROR(Wrong C++ compiler found; check the PATH!) ;;
esac
case "${AS}" in
   *avr*as*) ;;
   *) AC_MSG_ERROR(Wrong assembler found; check the PATH!) ;;
esac
case "${AR}" in
   *avr*ar*) ;;
   *) AC_MSG_ERROR(Wrong archiver found; check the PATH!) ;;
esac
case "${RANLIB}" in
   *avr*ranlib*) ;;
   *) AC_MSG_ERROR(Wrong ranlib found; check the PATH!) ;;
esac
case "${OBJCOPY}" in
   *avr*objcopy*) ;;
   *) AC_MSG_ERROR(Wrong objcopy found; check the PATH!) ;;
esac
case "${SIZE}" in
   *avr*size*) ;;
   *) AC_MSG_ERROR(Wrong size found; check the PATH!) ;;
esac

AX_CXX_COMPILE_STDCXX_11

AC_CONFIG_FILES([Makefile cores/arduino/Makefile])
AC_SUBST([RUNTIME_IDE_VERSION])

AC_OUTPUT