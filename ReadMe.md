# Introduction

DIY reflow solder plate controller design, where the actual plate connects with XT30 connector.<br>
Based on this [`PROJECT`](https://github.com/DerSpatz/PCB-reflow-solder-heat-plate)


All PDFs, images, and exports are under the [OUTPUTS](https://github.com/SantaClawzzz/TaltechHeat/tree/master/Outputs) folder

The BOM file is also there and the basket for it is [HERE](https://www.mouser.ee/Tools/SavedCart/Share?AccessID=80928401d5)

## Hardware:<br> 
- **20V 5A max**
- USB-C PD **(Power Delivery)** - `[STUSB4500]`
- MCU programmed with SWD - `[STM32F103C6]`
- 5V switching regulator - `[AP64060ZQ]`

## Pinout

|  User    |   Pin  |
|----------|--------|
|   BUT1   |  PC13  |
|   BUT2   |  PC14  |
|   PC15   |  PC15  |


| Signal     | Pin  | Function       |
|------------|------|----------------|
| SCL        | PB8  | I2C1_SCL       |
| SDA        | PB9  | I2C1_SDA       |
| PD_ALERT   | PB10 |                |
| PD_RST     | PB11 |                |
| PWM        | PB13 | TIM1_CH1N      |
| PD_GPIO    | PB14 |                |
| PD_ATTACH  | PB15 |                |
| VCC-DIV    | PA3  | ADC1_IN3       |
| TEMP1      | PA4  | ADC1_IN4       | 
| TEMP2      | PA5  | ADC1_IN5       |
| POWER_OK_3 | PA8  |                |
| UART1_RX   | PA9  | USART1_TX      |
| UART1_TX   | PA10 | USART1_RX      |
| SWDIO      | PA13 | SYS_JTMS-SWDIO |
| SWCLK      | PA14 | SYS_JTCK-SWCLK |

## Problems

- SWD pins not brought out to headers
- MOSFET too small, can't handle current (PD FET)
- PWM not on PWM capable pin
- Routing issues

- [More detail](https://docs.google.com/document/d/1i9aejrMOuASw6s5gDh6MXbNuGSY3eZ5T1xDJf5HSRbU/edit?tab=t.0)