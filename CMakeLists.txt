CMAKE_MINIMUM_REQUIRED(VERSION 3.10)

SET(CMAKE_SYSTEM_NAME Generic)
SET(CMAKE_SYSTEM_PROCESSOR cortex-m0-dual)
#SET(CMAKE_VERBOSE_MAKEFILE ON)

SET(CMAKE_EXPORT_COMPILE_COMMANDS ON)

SET(CMAKE_C_COMPILER "/usr/bin/arm-none-eabi-gcc")
SET(CMAKE_ASM_COMPILER "/usr/bin/arm-none-eabi-gcc")
SET(CMAKE_C_FLAGS " -march=armv6-m -mcpu=cortex-m0plus -mthumb -ffunction-sections -fdata-sections -Dgcc -O0 -gdwarf-2 -g")
SET(CMAKE_ASM_FLAGS " -c -march=armv6-m -mcpu=cortex-m0plus -mthumb -ffunction-sections -fdata-sections -x assembler-with-cpp -Wa,-mimplicit-it=thumb -ILibraries/pico-sdk/src/common/pico_stdlib/include -ILibraries/pico-sdk/src/rp2_common/hardware_gpio/include -ILibraries/pico-sdk/src/common/pico_base/include -ILibraries/generated/pico_base -ILibraries/pico-sdk/src/boards/include -ILibraries/pico-sdk/src/rp2_common/pico_platform/include -ILibraries/pico-sdk/src/rp2040/hardware_regs/include -ILibraries/pico-sdk/src/rp2_common/hardware_base/include -ILibraries/pico-sdk/src/rp2040/hardware_structs/include -ILibraries/pico-sdk/src/rp2_common/hardware_claim/include -ILibraries/pico-sdk/src/rp2_common/hardware_sync/include -ILibraries/pico-sdk/src/rp2_common/hardware_uart/include -ILibraries/pico-sdk/src/rp2_common/hardware_divider/include -ILibraries/pico-sdk/src/common/pico_time/include -ILibraries/pico-sdk/src/rp2_common/hardware_timer/include -ILibraries/pico-sdk/src/common/pico_sync/include -ILibraries/pico-sdk/src/common/pico_util/include -ILibraries/pico-sdk/src/rp2_common/pico_runtime/include -ILibraries/pico-sdk/src/rp2_common/hardware_clocks/include -ILibraries/pico-sdk/src/rp2_common/hardware_resets/include -ILibraries/pico-sdk/src/rp2_common/hardware_watchdog/include -ILibraries/pico-sdk/src/rp2_common/hardware_xosc/include -ILibraries/pico-sdk/src/rp2_common/hardware_pll/include -ILibraries/pico-sdk/src/rp2_common/hardware_vreg/include -ILibraries/pico-sdk/src/rp2_common/hardware_irq/include -ILibraries/pico-sdk/src/rp2_common/pico_printf/include -ILibraries/pico-sdk/src/rp2_common/pico_bootrom/include -ILibraries/pico-sdk/src/common/pico_bit_ops/include -ILibraries/pico-sdk/src/common/pico_divider/include -ILibraries/pico-sdk/src/rp2_common/pico_double/include -ILibraries/pico-sdk/src/rp2_common/pico_int64_ops/include -ILibraries/pico-sdk/src/rp2_common/pico_float/include -ILibraries/pico-sdk/src/common/pico_binary_info/include -ILibraries/pico-sdk/src/rp2_common/pico_stdio/include -ILibraries/pico-sdk/src/rp2_common/pico_stdio_uart/include -gdwarf-2")
SET(CMAKE_C_COMPILER_WORKS TRUE)

SET(CMAKE_CXX_COMPILER "/usr/bin/arm-none-eabi-g++")
SET(CMAKE_CXX_FLAGS " -march=armv6-m -mcpu=cortex-m0plus -mthumb -ffunction-sections -fdata-sections -Dgcc -O0 -gdwarf-2 -g")
SET(CMAKE_CXX_COMPILER_WORKS TRUE)

SET(CMAKE_OBJCOPY "/usr/bin/arm-none-eabi-objcopy")
SET(CMAKE_SIZE "/usr/bin/arm-none-eabi-size")

SET(CMAKE_EXE_LINKER_FLAGS " -march=armv6-m -mcpu=cortex-m0plus -mthumb -ffunction-sections -fdata-sections -Wl,--gc-sections,-Map=rt-thread.map,-cref,-u,Reset_Handler -T ${CMAKE_SOURCE_DIR}/link.ld -Wl,--build-id=none --specs=nosys.specs -Wl,--wrap=sprintf -Wl,--wrap=snprintf -Wl,--wrap=vsnprintf -Wl,--wrap=__clzsi2 -Wl,--wrap=__clzdi2 -Wl,--wrap=__ctzsi2 -Wl,--wrap=__ctzdi2 -Wl,--wrap=__popcountsi2 -Wl,--wrap=__popcountdi2 -Wl,--wrap=__clz -Wl,--wrap=__clzl -Wl,--wrap=__clzll -Wl,--wrap=__aeabi_idiv -Wl,--wrap=__aeabi_idivmod -Wl,--wrap=__aeabi_ldivmod -Wl,--wrap=__aeabi_uidiv -Wl,--wrap=__aeabi_uidivmod -Wl,--wrap=__aeabi_uldivmod -Wl,--wrap=__aeabi_dadd -Wl,--wrap=__aeabi_ddiv -Wl,--wrap=__aeabi_dmul -Wl,--wrap=__aeabi_drsub -Wl,--wrap=__aeabi_dsub -Wl,--wrap=__aeabi_cdcmpeq -Wl,--wrap=__aeabi_cdrcmple -Wl,--wrap=__aeabi_cdcmple -Wl,--wrap=__aeabi_dcmpeq -Wl,--wrap=__aeabi_dcmplt -Wl,--wrap=__aeabi_dcmple -Wl,--wrap=__aeabi_dcmpge -Wl,--wrap=__aeabi_dcmpgt -Wl,--wrap=__aeabi_dcmpun -Wl,--wrap=__aeabi_i2d -Wl,--wrap=__aeabi_l2d -Wl,--wrap=__aeabi_ui2d -Wl,--wrap=__aeabi_ul2d -Wl,--wrap=__aeabi_d2iz -Wl,--wrap=__aeabi_d2lz -Wl,--wrap=__aeabi_d2uiz -Wl,--wrap=__aeabi_d2ulz -Wl,--wrap=__aeabi_d2f -Wl,--wrap=sqrt -Wl,--wrap=cos -Wl,--wrap=sin -Wl,--wrap=tan -Wl,--wrap=atan2 -Wl,--wrap=exp -Wl,--wrap=log -Wl,--wrap=ldexp -Wl,--wrap=copysign -Wl,--wrap=trunc -Wl,--wrap=floor -Wl,--wrap=ceil -Wl,--wrap=round -Wl,--wrap=sincos -Wl,--wrap=asin -Wl,--wrap=acos -Wl,--wrap=atan -Wl,--wrap=sinh -Wl,--wrap=cosh -Wl,--wrap=tanh -Wl,--wrap=asinh -Wl,--wrap=acosh -Wl,--wrap=atanh -Wl,--wrap=exp2 -Wl,--wrap=log2 -Wl,--wrap=exp10 -Wl,--wrap=log10 -Wl,--wrap=pow -Wl,--wrap=powint -Wl,--wrap=hypot -Wl,--wrap=cbrt -Wl,--wrap=fmod -Wl,--wrap=drem -Wl,--wrap=remainder -Wl,--wrap=remquo -Wl,--wrap=expm1 -Wl,--wrap=log1p -Wl,--wrap=fma -Wl,--wrap=__aeabi_lmul -Wl,--wrap=__aeabi_fadd -Wl,--wrap=__aeabi_fdiv -Wl,--wrap=__aeabi_fmul -Wl,--wrap=__aeabi_frsub -Wl,--wrap=__aeabi_fsub -Wl,--wrap=__aeabi_cfcmpeq -Wl,--wrap=__aeabi_cfrcmple -Wl,--wrap=__aeabi_cfcmple -Wl,--wrap=__aeabi_fcmpeq -Wl,--wrap=__aeabi_fcmplt -Wl,--wrap=__aeabi_fcmple -Wl,--wrap=__aeabi_fcmpge -Wl,--wrap=__aeabi_fcmpgt -Wl,--wrap=__aeabi_fcmpun -Wl,--wrap=__aeabi_i2f -Wl,--wrap=__aeabi_l2f -Wl,--wrap=__aeabi_ui2f -Wl,--wrap=__aeabi_ul2f -Wl,--wrap=__aeabi_f2iz -Wl,--wrap=__aeabi_f2lz -Wl,--wrap=__aeabi_f2uiz -Wl,--wrap=__aeabi_f2ulz -Wl,--wrap=__aeabi_f2d -Wl,--wrap=sqrtf -Wl,--wrap=cosf -Wl,--wrap=sinf -Wl,--wrap=tanf -Wl,--wrap=atan2f -Wl,--wrap=expf -Wl,--wrap=logf -Wl,--wrap=ldexpf -Wl,--wrap=copysignf -Wl,--wrap=truncf -Wl,--wrap=floorf -Wl,--wrap=ceilf -Wl,--wrap=roundf -Wl,--wrap=sincosf -Wl,--wrap=asinf -Wl,--wrap=acosf -Wl,--wrap=atanf -Wl,--wrap=sinhf -Wl,--wrap=coshf -Wl,--wrap=tanhf -Wl,--wrap=asinhf -Wl,--wrap=acoshf -Wl,--wrap=atanhf -Wl,--wrap=exp2f -Wl,--wrap=log2f -Wl,--wrap=exp10f -Wl,--wrap=log10f -Wl,--wrap=powf -Wl,--wrap=powintf -Wl,--wrap=hypotf -Wl,--wrap=cbrtf -Wl,--wrap=fmodf -Wl,--wrap=dremf -Wl,--wrap=remainderf -Wl,--wrap=remquof -Wl,--wrap=expm1f -Wl,--wrap=log1pf -Wl,--wrap=fmaf -Wl,--wrap=malloc -Wl,--wrap=calloc -Wl,--wrap=free -Wl,--wrap=memcpy -Wl,--wrap=memset -Wl,--wrap=__aeabi_memcpy -Wl,--wrap=__aeabi_memset -Wl,--wrap=__aeabi_memcpy4 -Wl,--wrap=__aeabi_memset4 -Wl,--wrap=__aeabi_memcpy8 -Wl,--wrap=__aeabi_memset8 -Wl,--gc-sections -Wl,--wrap=printf -Wl,--wrap=vprintf -Wl,--wrap=puts -Wl,--wrap=putchar")

SET(CMAKE_CXX_STANDARD 14)
PROJECT(rtthread C CXX ASM)
INCLUDE_DIRECTORIES(
	applications
	rt-thread/components/libc/compilers/newlib
	rt-thread/components/libc/compilers/common/include
	libcpu
	rt-thread/libcpu/arm/common
	rt-thread/components/drivers/include
	board
	board/ports/lcd
	drivers
	rt-thread/components/finsh
	.
	rt-thread/include
	rt-thread/components/libc/posix/ipc
	rt-thread/components/libc/posix/io/epoll
	rt-thread/components/libc/posix/io/eventfd
	rt-thread/components/libc/posix/io/poll
	packages/raspberrypi-pico-sdk-latest/src/rp2_common/hardware_flash/include
	packages/raspberrypi-pico-sdk-latest/src/rp2_common/pico_multicore/include
	packages/raspberrypi-pico-sdk-latest/src/common/pico_stdlib/include
	packages/raspberrypi-pico-sdk-latest/src/rp2_common/hardware_gpio/include
	packages/raspberrypi-pico-sdk-latest/src/rp2_common/hardware_adc/include
	packages/raspberrypi-pico-sdk-latest/src/rp2_common/hardware_watchdog/include
	packages/raspberrypi-pico-sdk-latest/src/common/pico_base/include
	packages/raspberrypi-pico-sdk-latest/src/boards/include
	packages/raspberrypi-pico-sdk-latest/src/rp2_common/pico_platform/include
	packages/raspberrypi-pico-sdk-latest/src/rp2040/hardware_regs/include
	packages/raspberrypi-pico-sdk-latest/src/rp2_common/hardware_base/include
	packages/raspberrypi-pico-sdk-latest/src/rp2040/hardware_structs/include
	packages/raspberrypi-pico-sdk-latest/src/rp2_common/hardware_claim/include
	packages/raspberrypi-pico-sdk-latest/src/rp2_common/hardware_sync/include
	packages/raspberrypi-pico-sdk-latest/src/rp2_common/hardware_uart/include
	packages/raspberrypi-pico-sdk-latest/src/rp2_common/hardware_dma/include
	packages/raspberrypi-pico-sdk-latest/src/rp2_common/hardware_spi/include
	packages/raspberrypi-pico-sdk-latest/src/rp2_common/hardware_i2c/include
	packages/raspberrypi-pico-sdk-latest/src/rp2_common/hardware_pwm/include
	packages/raspberrypi-pico-sdk-latest/src/rp2_common/hardware_divider/include
	packages/raspberrypi-pico-sdk-latest/src/common/pico_time/include
	packages/raspberrypi-pico-sdk-latest/src/rp2_common/hardware_timer/include
	packages/raspberrypi-pico-sdk-latest/src/common/pico_sync/include
	packages/raspberrypi-pico-sdk-latest/src/common/pico_util/include
	packages/raspberrypi-pico-sdk-latest/src/rp2_common/pico_runtime/include
	packages/raspberrypi-pico-sdk-latest/src/rp2_common/hardware_clocks/include
	packages/raspberrypi-pico-sdk-latest/src/rp2_common/hardware_resets/include
	packages/raspberrypi-pico-sdk-latest/src/rp2_common/hardware_xosc/include
	packages/raspberrypi-pico-sdk-latest/src/rp2_common/hardware_pll/include
	packages/raspberrypi-pico-sdk-latest/src/rp2_common/hardware_vreg/include
	packages/raspberrypi-pico-sdk-latest/src/rp2_common/hardware_irq/include
	packages/raspberrypi-pico-sdk-latest/src/rp2_common/pico_printf/include
	packages/raspberrypi-pico-sdk-latest/src/rp2_common/pico_bootrom/include
	packages/raspberrypi-pico-sdk-latest/src/common/pico_bit_ops/include
	packages/raspberrypi-pico-sdk-latest/src/common/pico_divider/include
	packages/raspberrypi-pico-sdk-latest/src/rp2_common/pico_double/include
	packages/raspberrypi-pico-sdk-latest/src/rp2_common/pico_int64_ops/include
	packages/raspberrypi-pico-sdk-latest/src/rp2_common/pico_float/include
	packages/raspberrypi-pico-sdk-latest/src/common/pico_binary_info/include
	packages/raspberrypi-pico-sdk-latest/src/rp2_common/pico_stdio/include
	packages/raspberrypi-pico-sdk-latest/src/rp2_common/pico_stdio_uart/include
	packages/raspberrypi-pico-sdk-latest/src/rp2_common/pico_malloc/include
	packages/raspberrypi-pico-sdk-latest/src/rp2_common/boot_stage2/include
)

ADD_DEFINITIONS(
	-DPICO_BIT_OPS_PICO=1
	-DPICO_BUILD=1
	-DPICO_COPY_TO_RAM=0
	-DPICO_CXX_ENABLE_EXCEPTIONS=0
	-DPICO_DIVIDER_HARDWARE=1
	-DPICO_DOUBLE_PICO=1
	-DPICO_FLOAT_PICO=1
	-DPICO_INT64_OPS_PICO=1
	-DPICO_MEM_OPS_PICO=1
	-DPICO_NO_BINARY_INFO
	-DPICO_NO_FLASH=0
	-DPICO_NO_HARDWARE=0
	-DPICO_NO_PROGRAM_INFO
	-DPICO_ON_DEVICE=1
	-DPICO_PRINTF_PICO=1
	-DPICO_STDIO_UART=1
	-DPICO_USE_BLOCKED_RAM=0
	-DRT_USING_LIBC
	-DRT_USING_NEWLIBC
	-D_POSIX_C_SOURCE=1
	-D__RTTHREAD__
)

SET(PROJECT_SOURCES
	applications/main.c
	rt-thread/components/libc/compilers/common/cctype.c
	rt-thread/components/libc/compilers/common/cstdlib.c
	rt-thread/components/libc/compilers/common/cstring.c
	rt-thread/components/libc/compilers/common/ctime.c
	rt-thread/components/libc/compilers/common/cunistd.c
	rt-thread/components/libc/compilers/common/cwchar.c
	rt-thread/components/libc/compilers/newlib/syscalls.c
	libcpu/context_gcc.S
	libcpu/cpuport.c
	rt-thread/libcpu/arm/common/div0.c
	rt-thread/libcpu/arm/common/showmem.c
	rt-thread/components/drivers/core/device.c
	rt-thread/components/drivers/ipc/completion.c
	rt-thread/components/drivers/ipc/dataqueue.c
	rt-thread/components/drivers/ipc/pipe.c
	rt-thread/components/drivers/ipc/ringblk_buf.c
	rt-thread/components/drivers/ipc/ringbuffer.c
	rt-thread/components/drivers/ipc/waitqueue.c
	rt-thread/components/drivers/ipc/workqueue.c
	rt-thread/components/drivers/misc/pin.c
	rt-thread/components/drivers/serial/serial.c
	board/board.c
	drivers/drv_gpio.c
	drivers/drv_uart.c
	rt-thread/components/finsh/cmd.c
	rt-thread/components/finsh/shell.c
	rt-thread/components/finsh/msh.c
	rt-thread/components/finsh/msh_parse.c
	rt-thread/src/clock.c
	rt-thread/src/components.c
	rt-thread/src/idle.c
	rt-thread/src/ipc.c
	rt-thread/src/irq.c
	rt-thread/src/kservice.c
	rt-thread/src/mem.c
	rt-thread/src/mempool.c
	rt-thread/src/object.c
	rt-thread/src/scheduler_up.c
	rt-thread/src/thread.c
	rt-thread/src/timer.c
	packages/raspberrypi-pico-sdk-latest/src/rp2_common/hardware_i2c/i2c.c
	packages/raspberrypi-pico-sdk-latest/src/rp2_common/hardware_divider/divider.S
	packages/raspberrypi-pico-sdk-latest/src/rp2_common/pico_standard_link/binary_info.c
	packages/raspberrypi-pico-sdk-latest/src/rp2_common/pico_float/float_math.c
	packages/raspberrypi-pico-sdk-latest/src/rp2_common/hardware_watchdog/watchdog.c
	packages/raspberrypi-pico-sdk-latest/src/rp2_common/pico_mem_ops/mem_ops_aeabi.S
	packages/raspberrypi-pico-sdk-latest/src/rp2_common/hardware_sync/sync.c
	packages/raspberrypi-pico-sdk-latest/src/rp2_common/hardware_xosc/xosc.c
	packages/raspberrypi-pico-sdk-latest/src/rp2_common/hardware_irq/irq_handler_chain.S
	packages/raspberrypi-pico-sdk-latest/src/common/pico_sync/lock_core.c
	packages/raspberrypi-pico-sdk-latest/src/common/pico_sync/sem.c
	packages/raspberrypi-pico-sdk-latest/src/rp2_common/hardware_claim/claim.c
	packages/raspberrypi-pico-sdk-latest/src/rp2_common/hardware_adc/adc.c
	packages/raspberrypi-pico-sdk-latest/src/rp2_common/hardware_timer/timer.c
	packages/raspberrypi-pico-sdk-latest/src/rp2_common/hardware_irq/irq.c
	packages/raspberrypi-pico-sdk-latest/src/rp2_common/pico_printf/printf.c
	packages/raspberrypi-pico-sdk-latest/src/rp2_common/pico_divider/divider.S
	packages/raspberrypi-pico-sdk-latest/src/common/pico_time/time.c
	packages/raspberrypi-pico-sdk-latest/src/rp2_common/pico_double/double_v1_rom_shim.S
	packages/raspberrypi-pico-sdk-latest/src/rp2_common/pico_double/double_init_rom.c
	packages/raspberrypi-pico-sdk-latest/src/common/pico_sync/critical_section.c
	packages/raspberrypi-pico-sdk-latest/src/common/pico_time/timeout_helper.c
	packages/raspberrypi-pico-sdk-latest/src/rp2_common/pico_runtime/runtime.c
	packages/raspberrypi-pico-sdk-latest/src/rp2_common/hardware_pll/pll.c
	packages/raspberrypi-pico-sdk-latest/src/rp2_common/pico_stdio/stdio.c
	packages/raspberrypi-pico-sdk-latest/bs2_default_padded_checksummed.S
	packages/raspberrypi-pico-sdk-latest/src/rp2_common/pico_int64_ops/pico_int64_ops_aeabi.S
	packages/raspberrypi-pico-sdk-latest/src/rp2_common/hardware_gpio/gpio.c
	packages/raspberrypi-pico-sdk-latest/src/rp2_common/hardware_flash/flash.c
	packages/raspberrypi-pico-sdk-latest/src/rp2_common/pico_bootrom/bootrom.c
	packages/raspberrypi-pico-sdk-latest/src/common/pico_sync/mutex.c
	packages/raspberrypi-pico-sdk-latest/src/rp2_common/pico_standard_link/crt0.S
	packages/raspberrypi-pico-sdk-latest/src/common/pico_util/queue.c
	packages/raspberrypi-pico-sdk-latest/src/rp2_common/pico_malloc/pico_malloc.c
	packages/raspberrypi-pico-sdk-latest/src/rp2_common/pico_float/float_init_rom.c
	packages/raspberrypi-pico-sdk-latest/src/rp2_common/pico_double/double_aeabi.S
	packages/raspberrypi-pico-sdk-latest/src/rp2_common/pico_double/double_math.c
	packages/raspberrypi-pico-sdk-latest/src/rp2_common/pico_platform/platform.c
	packages/raspberrypi-pico-sdk-latest/src/common/pico_util/pheap.c
	packages/raspberrypi-pico-sdk-latest/src/rp2_common/hardware_clocks/clocks.c
	packages/raspberrypi-pico-sdk-latest/src/rp2_common/pico_stdio_uart/stdio_uart.c
	packages/raspberrypi-pico-sdk-latest/src/rp2_common/hardware_vreg/vreg.c
	packages/raspberrypi-pico-sdk-latest/src/rp2_common/pico_standard_link/new_delete.cpp
	packages/raspberrypi-pico-sdk-latest/src/rp2_common/pico_bit_ops/bit_ops_aeabi.S
	packages/raspberrypi-pico-sdk-latest/src/rp2_common/pico_stdlib/stdlib.c
	packages/raspberrypi-pico-sdk-latest/src/rp2_common/pico_float/float_aeabi.S
	packages/raspberrypi-pico-sdk-latest/src/rp2_common/hardware_spi/spi.c
	packages/raspberrypi-pico-sdk-latest/src/rp2_common/pico_multicore/multicore.c
	packages/raspberrypi-pico-sdk-latest/src/rp2_common/hardware_uart/uart.c
	packages/raspberrypi-pico-sdk-latest/src/rp2_common/hardware_dma/dma.c
	packages/raspberrypi-pico-sdk-latest/src/rp2_common/pico_float/float_v1_rom_shim.S
	packages/raspberrypi-pico-sdk-latest/src/common/pico_util/datetime.c
)

LINK_DIRECTORIES(
)

LINK_LIBRARIES(
	c
	m
)

ADD_EXECUTABLE(${CMAKE_PROJECT_NAME}.elf ${PROJECT_SOURCES})
ADD_CUSTOM_COMMAND(TARGET ${CMAKE_PROJECT_NAME}.elf POST_BUILD 
COMMAND ${CMAKE_OBJCOPY} -O binary ${CMAKE_PROJECT_NAME}.elf ${CMAKE_PROJECT_NAME}.bin COMMAND ${CMAKE_SIZE} ${CMAKE_PROJECT_NAME}.elf)