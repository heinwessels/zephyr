# SPDX-License-Identifier: Apache-2.0

zephyr_syscall_header(${ZEPHYR_BASE}/include/zephyr/drivers/hwinfo.h)

zephyr_library()

zephyr_library_sources_ifdef(CONFIG_USERSPACE          hwinfo_handlers.c)
zephyr_library_sources_ifdef(CONFIG_HWINFO             hwinfo_weak_impl.c)
zephyr_library_sources_ifdef(CONFIG_HWINFO_SHELL       hwinfo_shell.c)

# zephyr-keep-sorted-start
zephyr_library_sources_ifdef(CONFIG_HWINFO_AMBIQ       hwinfo_ambiq.c)
zephyr_library_sources_ifdef(CONFIG_HWINFO_ANDES       hwinfo_andes.c)
zephyr_library_sources_ifdef(CONFIG_HWINFO_CC13XX_CC26XX hwinfo_cc13xx_cc26xx.c)
zephyr_library_sources_ifdef(CONFIG_HWINFO_ESP32       hwinfo_esp32.c)
zephyr_library_sources_ifdef(CONFIG_HWINFO_GECKO       hwinfo_gecko.c)
zephyr_library_sources_ifdef(CONFIG_HWINFO_IMXRT       hwinfo_imxrt.c)
zephyr_library_sources_ifdef(CONFIG_HWINFO_LITEX       hwinfo_litex.c)
zephyr_library_sources_ifdef(CONFIG_HWINFO_MAX32       hwinfo_max32.c)
zephyr_library_sources_ifdef(CONFIG_HWINFO_MCUX_RCM    hwinfo_mcux_rcm.c)
zephyr_library_sources_ifdef(CONFIG_HWINFO_MCUX_SIM    hwinfo_mcux_sim.c)
zephyr_library_sources_ifdef(CONFIG_HWINFO_MCUX_SRC    hwinfo_mcux_src.c)
zephyr_library_sources_ifdef(CONFIG_HWINFO_MCUX_SRC_V2 hwinfo_mcux_src_rev2.c)
zephyr_library_sources_ifdef(CONFIG_HWINFO_MCUX_SYSCON hwinfo_mcux_syscon.c)
zephyr_library_sources_ifdef(CONFIG_HWINFO_NRF         hwinfo_nrf.c)
zephyr_library_sources_ifdef(CONFIG_HWINFO_NUMAKER     hwinfo_numaker.c)
zephyr_library_sources_ifdef(CONFIG_HWINFO_NUMAKER_RMC hwinfo_numaker_rmc.c)
zephyr_library_sources_ifdef(CONFIG_HWINFO_PSOC6       hwinfo_psoc6.c)
zephyr_library_sources_ifdef(CONFIG_HWINFO_RENESAS_RA  hwinfo_renesas_ra.c)
zephyr_library_sources_ifdef(CONFIG_HWINFO_RPI_PICO    hwinfo_rpi_pico.c)
zephyr_library_sources_ifdef(CONFIG_HWINFO_RW61X       hwinfo_rw61x.c)
zephyr_library_sources_ifdef(CONFIG_HWINFO_SAM         hwinfo_sam.c)
zephyr_library_sources_ifdef(CONFIG_HWINFO_SAM0        hwinfo_sam0.c)
zephyr_library_sources_ifdef(CONFIG_HWINFO_SAM4L       hwinfo_sam4l.c)
zephyr_library_sources_ifdef(CONFIG_HWINFO_SAM_RSTC    hwinfo_sam_rstc.c)
zephyr_library_sources_ifdef(CONFIG_HWINFO_SILABS_S2   hwinfo_silabs_series2.c)
zephyr_library_sources_ifdef(CONFIG_HWINFO_SMARTBOND   hwinfo_smartbond.c)
zephyr_library_sources_ifdef(CONFIG_HWINFO_STM32       hwinfo_stm32.c)
# zephyr-keep-sorted-stop
