obj-$(CONFIG_MTD_RALINK)	+= ralink-flash.o
obj-$(CONFIG_MTD_SPI_RALINK)	+= rt_spi.o
obj-$(CONFIG_MTD_SPINAND_ECONET)+= rt_nand.o

rt_spi-objs = ralink_spi_bbu.o

ifeq ($(CONFIG_MTD_SPINAND_ECONET),y)
EXTRA_CFLAGS += -DTCSUPPORT_NAND_BMT
rt_nand-objs += en75xx_nand/bmt.o
rt_nand-objs += en75xx_nand/spi_controller.o
rt_nand-objs += en75xx_nand/spi_nand_flash.o
rt_nand-objs += en75xx_nand/spi_nand_flash_table.o
endif
