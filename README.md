A simple tool to determine various clocks frequency on AST2x00 chips.

## Usage

Just run it without parameters.

It will print the following clock information:

* for AST2400: CPU, AHB, PCLK.
* for AST2500: CPU, MEM, DPLL, AHB, PCLK, BCLK, HCLK.
* for AST2600: CPU, MEM, APLL, EPLL, DPLL, AHB, ECC/RSA, PCLK, BCLK, AXI, HCLK.

## Requirements

* `bash` should be able to run scripts such as this one.
* `bash` should be able to calculate expressions like `$((0x1234567 >> 8 & 7))` and `$((1234 / 56))`.
* `CLKIN` should be 24 MHz for AST2500 and 25 MHz for AST2600.
* `devmem` utility should be available.
* `/dev/mem` should exist (e.g. there should be `CONFIG_DEVMEM_BOOTPARAM=n` in kernel config for OpenBMC).
* `/sys/devices/soc0/family` should contain CPU model (either `AST2400`, `AST2500`, or `AST2600`).