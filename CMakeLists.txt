cmake_minimum_required(VERSION 3.5)

project(mimxrt1170-evk)

add_definitions("
    -DCPU_MIMXRT1176DVMAA_cm7
    -DSDK_DEBUGCONSOLE=1
    -DXIP_EXTERNAL_FLASH=1
    -DXIP_BOOT_HEADER_ENABLE=1
    -DSERIAL_PORT_TYPE_UART=1
    -DSDK_OS_FREE_RTOS
    -DMCUXPRESSO_SDK
    -DCPU_MIMXRT1176DVMAA
    -DCR_INTEGER_PRINTF
    -D__MCUXPRESSO
    -D__USE_CMSIS
    -DDEBUG_CONSOLE_RX_ENABLE=0
    -DNDEBUG
    -D__NEWLIB__
    ")

add_subdirectory(app)
add_subdirectory(mcrt)
