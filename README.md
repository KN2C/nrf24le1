# Depends

This driver depends of entrance like this:

```c
static struct spi_board_info spi_devices[] = {
	{
		.modalias = "nrf24le1",
		.chip_select = 0,
		.max_speed_hz = 4500*1000,
		.bus_num = 1,
	},
};

at91_add_device_spi(spi_devices, ARRAY_SIZE(spi_devices));
```

at board definition file, who normaly stay in:
```
arch/arm/mach-at91
```

# Build

```
KERNELDIR=<path_to_your_kernel> make
```

# Doc

* For documentacion about nrf24le1 look nordic oficial web site:
<http://www.nordicsemi.com/eng/Products/2.4GHz-RF/nRF24LE1>
* Useful tools: <http://www.glomationinc.com/support.html>
