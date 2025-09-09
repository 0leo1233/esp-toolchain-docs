## Choose your target

[<img alt="ESP32" width="20%" src="imgs/esp32.png" />](esp32/README.md)
[<img alt="ESP32-S3" width="20%" src="imgs/esp32s3.png" />](esp32s3/README.md)
[<img alt="ESP32-C3" width="20%" src="imgs/esp32c3.png" />](esp32c3/README.md)

## Supported features

|    Feature \ Target   | ESP32 | ESP32-S3 | ESP32-C3 | Notes                                                                                     |
|:---------------------:|:-----:|:--------:|:--------:|-------------------------------------------------------------------------------------------|
|     Dual-Core CPU     |   ✅   |     ✅    |    N/A   |                                                                                           |
|          UART         |   ✅   |     ✅    |     ✅    |                                                                                           |
|    Interrupt matrix   |   ✅   |     ✅    |     ✅    |                                                                                           |
|       GPIO strap      |   ✅   |     ✅    |     ✅    |                                                                                           |
|     NOR Flash SPI     |   ✅   |     ✅    |     ✅    |                                                                                           |
|     NOR Flash MMU     |   ✅   |    ✅*    |     ✅    | ESP32-S3 uses the host's hardware MMU for better emulation                                |
|  NOR Flash encryption |   ✅   |     ✅    |     ✅    |                                                                                           |
|       PSRAM QPI       |   ✅   |     ✅    |    N/A   |                                                                                           |
|       PSRAM OPI       |   ✅*  |     ✅    |    N/A   | ESP32 doesn't support Octal PSRAM on the real hardware                                    |
|       PSRAM MMU       |  N/A  |    ✅*    |    N/A   | ESP32-S3 uses the host's hardware MMU for better emulation                                |
|         eFuse         |   ✅   |     ✅    |     ✅    |                                                                                           |
|          RNG          |   ✅   |     ✅    |     ✅    |                                                                                           |
|          GDMA         |  N/A  |     ✅    |     ✅    |                                                                                           |
|          AES          |   ✅   |     ✅    |     ✅    |                                                                                           |
|          SHA          |   ✅   |     ✅    |     ✅    |                                                                                           |
|          RSA          |   ✅   |     ✅    |     ✅    |                                                                                           |
|          HMAC         |  N/A  |     ✅    |     ✅    |                                                                                           |
|   Digital Signature   |  N/A  |     ✅    |     ✅    |                                                                                           |
|        SysTimer       |  N/A  |     ✅    |     ✅    |                                                                                           |
|      Timer Groups     |   ✅   |     ✅    |     ✅    |                                                                                           |
|        TWAI/CAN       |   ✅   |     ✅    |     ✅    |                                                                                           |
|         SD/MMC        |   ✅   |     ❌    |    N/A   |                                                                                           |
| Ethernet* (OpenCores) |   ✅   |     ✅    |     ✅    | This is not a real hardware peripheral, it is used to have networking in emulated targets |
|    RGB Framebuffer*   |   ✅   |     ✅    |     ✅    | This is not a real hardware peripheral, it is used to simplify GUI testing                |
|       DirectBoot      |  N/A  |    N/A   |     ✅    |                                                                                           |
|          LEDC         |   ✅   |     ❌    |     ❌    |                                                                                           |
|          Wi-Fi        |   ❌   |     ❌    |     ❌    | The Ethernet controller can be used for networking instead                                |
|       Bluetooth       |   ❌   |     ❌    |     ❌    |                                                                                           |
|          USB          |   ❌   |     ❌    |     ❌    |                                                                                           |
|          RMT          |   ❌   |     ❌    |     ❌    |                                                                                           |
|         GP SPI        |   ❌   |     ❌    |     ❌    |                                                                                           |
|          I2C          |   ❌   |     ❌    |     ❌    |                                                                                           |
|          I2S          |   ❌   |     ❌    |     ❌    |                                                                                           |
|   ULP (co-processor)  |   ❌   |     ❌    |     ❌    |                                                                                           |
|  GPIO matrix / IOMUX  |   ❌   |     ❌    |     ❌    |                                                                                           |

## About Espressif QEMU fork

[Espressif's QEMU project](https://github.com/espressif/qemu) contains a fork of QEMU with patches for Espressif chips support. We hope that these patches will eventually be mature enough to become part of the upstream QEMU project.

At the moment, Espressif does not provide support for QEMU. We appreciate issue reports but keep in mind that our response may be delayed. We will likely not be able to help with issues that require extensive troubleshooting or don't have a straightforward way to reproduce them. We will also likely not be able to help with particular use cases which aren't supported yet (e.g. due to missing emulation of some peripherals).

The main branch of that repository is `esp-develop`. This branch will often be rebased on top of the upstream master branch and force-pushed. If you wish to submit a non-trivial PR, please open an issue first so that we can avoid making conflicting changes.

## Disclaimer

```
This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU General Public License for more details.
```
