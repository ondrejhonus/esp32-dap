# ESP-32 Digital Audio Player


## Parts
- [ESP32-S3 Chip](https://www.aliexpress.com/item/1005006214506085.html?spm=a2g0o.cart.0.0.2dae38daCLOcHa&mp=1&pdp_npi=6%40dis%21CZK%21CZK%2099.49%21CZK%2099.49%21%21CZK%2099.49%21%21%21%40211b653717729246377494041e4aca%2112000036313776249%21ct%21CZ%214581780593%21%212%210%21&pdp_ext_f=%7B%22cart2PdpParams%22%3A%7B%22pdpBusinessMode%22%3A%22retail%22%7D%7D)
- [PCM5102A (3.5mm Jack DAC)](https://www.aliexpress.com/item/1005009648364414.html?spm=a2g0o.cart.0.0.5f0138dabrOkGC&mp=1&pdp_npi=6%40dis%21CZK%21CZK%2050.54%21CZK%2021.27%21%21CZK%2021.27%21%21%21%40211b819117729178844098157e9d20%2112000049761355767%21ct%21CZ%214581780593%21%211%210%21)
- [ILI9341 2.8" Display (No PCB)](https://www.aliexpress.com/item/1005005780989629.html?spm=a2g0o.cart.0.0.2f3838daYu06pI&mp=1&pdp_npi=6%40dis%21CZK%21CZK%20107.87%21CZK%20107.87%21%21CZK%20107.87%21%21%21%40211b441e17729282846866071ec813%2112000034331367522%21ct%21CZ%214581780593%21%212%210%21&pdp_ext_f=%7B%22cart2PdpParams%22%3A%7B%22pdpBusinessMode%22%3A%22retail%22%7D%7D)
- [FPC Display Connector](https://www.aliexpress.com/item/1005010768274556.html?spm=a2g0o.cart.0.0.2f3838darn1ht2&mp=1&pdp_npi=6%40dis%21CZK%21CZK%20121.79%21CZK%2057.26%21%21CZK%2057.26%21%21%21%40211b441e17729282469775409ec813%2112000053447353396%21ct%21CZ%214581780593%21%211%210%21)
- [SDIO MicroSD Slot](https://www.aliexpress.com/item/1005009878687360.html?mp=1&pdp_npi=6%40dis%21CZK%21CZK%20142.10%21CZK%20142.10%21%21CZK%20142.10%21%21%21%40210385bb17729196673161345e119f%2112000056479644740%21ct%21CZ%214581780593%21%211%210%21)
- [128GB MicroSD Card](https://www.aliexpress.com/item/1005001617961938.html?spm=a2g0o.productlist.main.4.24f47d38jULNJU&algo_pvid=480e5718-7814-473d-adbd-cef07a61e630&algo_exp_id=480e5718-7814-473d-adbd-cef07a61e630-1&pdp_ext_f=%7B%22order%22%3A%22167105%22%2C%22spu_best_type%22%3A%22price%22%2C%22eval%22%3A%221%22%2C%22fromPage%22%3A%22search%22%7D&pdp_npi=6%40dis%21CZK%21143.11%21132.37%21%21%216.66%216.16%21%40211b813f17729197365088656e7edd%2112000037146031431%21sea%21CZ%214581780593%21ACX%211%210%21n_tag%3A-29919%3Bd%3Ad3716609%3Bm03_new_user%3A-29894%3BpisId%3A5000000197849194&curPageLogUid=JAi66EDHC6fK&utparam-url=scene%3Asearch%7Cquery_from%3A%7Cx_object_id%3A1005001617961938%7C_p_origin_prod%3A)
- [5-way button](https://www.aliexpress.com/item/1005001591225897.html?spm=a2g0o.cart.0.0.2dae38daCLOcHa&mp=1&pdp_npi=6%40dis%21CZK%21CZK%20103.14%21CZK%20103.14%21%21CZK%20103.14%21%21%21%40211b653717729246377494041e4aca%2112000016715372322%21ct%21CZ%214581780593%21%211%210%21)
- [Li-Po Battery](https://www.aliexpress.com/item/1005009590723370.html?spm=a2g0o.cart.0.0.2dae38daCLOcHa&mp=1&pdp_npi=6%40dis%21CZK%21CZK%20624.67%21CZK%20218.63%21%21CZK%20218.63%21%21%21%40211b653717729246377494041e4aca%2112000049557506746%21ct%21CZ%214581780593%21%211%210%21)
- [Battery charging regulator (U also need 1.2k ohm resistor)](https://www.aliexpress.com/item/1005007439657191.html?spm=a2g0o.cart.0.0.2dae38daCLOcHa&mp=1&pdp_npi=6%40dis%21CZK%21CZK%2042.98%21CZK%2042.98%21%21CZK%2042.98%21%21%21%40211b653717729246377494041e4aca%2112000040759803425%21ct%21CZ%214581780593%21%211%210%21&pdp_ext_f=%7B%22cart2PdpParams%22%3A%7B%22pdpBusinessMode%22%3A%22retail%22%7D%7D)
- [USB-C header with 5.1K](https://www.aliexpress.com/item/1005009993484503.html?spm=a2g0o.cart.0.0.73be38davhnDor&mp=1&pdp_npi=6%40dis%21CZK%21CZK%2043.42%21CZK%2038.63%21%21CZK%2038.63%21%21%21%402103919917729267772442961e22fa%2112000050785974007%21ct%21CZ%214581780593%21%211%210%21)
- LEDs (Power / Charging indicators)

### For watching battery percentage
- 2x 100 K ohm resistor
    - One to Battery(+), one to ground, the middle point to ADC on esp32 (eg. GPIO4)
- 1x Filter Capacitor for clean power (0.1uF)

## Connections

### Custom PCB wiring

| Function          | ESP32-S3 Pin (GPIO) | Target Component & Pin      | Note                                      |
|:------------------|:--------------------|:----------------------------|:------------------------------------------|
| **Power (3.3V)** | **3V3** | all components (VCC / VDD / +)     | from AP2112K-3.3V                |
| **Ground** | **GND** | everytihing (GND / -)           | -                      |
| **Display: SCK** | **GPIO 18** | FPC Pin 12                  |                                  |
| **Display: MOSI** | **GPIO 17** | FPC Pin 11                  |            |
| **Display: CS** | **GPIO 10** | FPC Pin 8                   |                                |
| **Display: DC** | **GPIO 9** | FPC Pin 9                   |                   |
| **Display: RESET**| **GPIO 8** | FPC Pin 10                  |                             |
| **Audio: BCK** | **GPIO 1** | DAC: BCK                    |                              |
| **Audio: DIN** | **GPIO 41** | DAC: DIN                    |                                |
| **Audio: LRCK** | **GPIO 42** | DAC: LRCK                   |               |
| **Audio: SCK** | **GND** | DAC: SCK                   |    so it doesnt use esp32 clock           | 
| **microSD: CLK** | **GPIO 14** | SD: CLK                     |                                 |
| **microSD: CMD** | **GPIO 15** | SD: CMD                     |                               |
| **microSD: D0** | **GPIO 2** | SD: D0                      | same as DAC DIN,       |
| **microSD: D1** | **GPIO 4** | SD: D1                      |                                |
| **microSD: D2** | **GPIO 12** | SD: D2                      | same as SPI SCK         |
| **microSD: D3** | **GPIO 13** | SD: D3                      |              |
| **USB Data -** | **GPIO 19** | USB-C: D-                   |                   |
| **USB Data +** | **GPIO 20** | USB-C: D+                   |                   |
| **Battery Check** | **GPIO 5** | node A, voltage divider [here](#for-watching-battery-percentage)    |  0V–3.3V for bat percentabe         |

### 5-way button

| Button           | ESP32-S3 Pin | Mode / Logic        | Function                             |
|:-----------------|:-------------|:--------------------|:-------------------------------------|
| **Up** | **GPIO 6** | internal pull-up    | Scroll Up / Vol Up (Hold)            |
| **Down** | **GPIO 7** | internal pull-up    | Scroll Down / Vol Down (Hold)        |
| **Prev** | **GPIO 16** | internal pull-up    | Previous Song / Back (Hold)          |
| **Next** | **GPIO 21** | internal pull-up    | Next Song                            |
| **Play / Pause** | **GPIO 3** | internal pull-up    | Play-Pause / Shutdown (Hold)         |

### Boring stuff coz i chose a bare esp chip

| Component        | Connection 1       | Connection 2       | Purpose                              |
|:-----------------|:-------------------|:-------------------|:-------------------------------------|
| **EN Resistor** | ESP32 Pin: EN      | 3.3V (10kΩ)        | prevents shutdown (pull-up)         |
| **Boot Resistor**| ESP32 Pin: GPIO 0  | 3.3V (10kΩ)        | prevents random boot loops           |

### esp controls / indicators

| Item              | Connection A | Connection B                | Note                                  |
|:------------------|:-------------|:----------------------------|:------------------------------------------|
| **Charging LED** | USB 5V (1kΩ R) | TP4056 pin 7 (CHRG)         | prolly red LED                  |
| **Full LED** | USB 5V (1kΩ) | TP4056 Pin 6 (STDBY)        | green when battery full?                     |
| **Reset Button** | EN Pin       | GND (momentary)             | restart esp                       |
| **Boot Button** | GPIO 0       | GND (momentary)             |  Flash Mode                 |