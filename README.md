# NSSFC

NSSFC is an FPV flight controller made with the STM32F405 and it has an IMU, Barometric pressure sensor and a magnetometer. It uses the betaflight as firmware(thus no firmware directory in this repository). The package is a typical 37mmx37mm.  

View the board on [KiCanvas](https://kicanvas.org/?repo=https%3A%2F%2Fgithub.com%2FKeyaan-07%2FNSSFC%2Ftree%2Fmain%2Fhardware)  

We made it to learn more about Flight controllers and make PCBs in a small area, especially something like 37x37mm!  


![3d render](/images/render-3d.png)
![pcb](https://cdn.hackclub.com/01a0ba9c-c613-7759-ba2e-12fc01e75e84/paste-1789837229892.png)  
<!-- ![kicad-render](https://cdn.hackclub.com/01a0baac-9bc2-7ff9-bda2-ef1c0acee228/paste-1789838268458.png) -->
![kicad-render](https://cdn.hackclub.com/01a0baad-3077-7e57-80d2-fea76b8812c0/paste-1789838306085.png)
![schematic](/images/nssfc.svg)  


## How to assemble:  
1. Order PCBs and components from the [/hardware/production](/hardware/production/) folder and order them from your supplier and PCB fab. Don't forget to get a stencil along with your PCB!
2. Place the PCB on a flat surface and place the stencil over it. 
3. Use medium-temp solder paste to put the soldermask pattern over the PCB. 
4. Carefully place all the components, use the [ibom](/hardware/bom/ibom.html) for smooth placement. 
5. Solder it in a reflow-oven or a hotplate!
6. You're done!!

## How to flash firmware. 
1. Hold the BOOT0 button and put in the USB into your computer. 
2. Use [betaflight web configurator](https://app.betaflight.com/) to flash the lastest build. [here](https://github.com/betaflight/betaflight/releases/download/2026.6.2/betaflight_2026.6.2_STM32F405.hex) is the latest build!


# BOM
|Designator                                                |Function        |Value           |Footprint                               |Quantity|Price        |Amount |Link                                              |
|----------------------------------------------------------|----------------|----------------|----------------------------------------|--------|-------------|-------|--------------------------------------------------|
|PCB                                                       |                |                |                                        |5       |             |2      |https://jlcpcb.com/                               |
|Stencil                                                   |                |                |                                        |1       |             |3.1    |https://jlcpcb.com/                               |
|C1, C16, C2                                               |Capacitor       |2.2u            |402                                     |3       |0.0054       |0.0162 |https://www.lcsc.com/product-detail/C12530.html   |
|C10                                                       |Capacitor       |1u              |402                                     |1       |0.047        |0.047  |https://www.lcsc.com/product-detail/C1518208.html |
|C11                                                       |Capacitor       |4.7u            |402                                     |1       |0.0275       |0.0275 |https://www.lcsc.com/product-detail/C20624278.html|
|C12, C13, C14, C15, C17, C19, C23, C25, C5, C6, C7, C8, C9|Capacitor       |100n            |402                                     |13      |0.0045       |0.0585 |https://www.lcsc.com/product-detail/C5182432.html |
|C20                                                       |Capacitor       |22u             |805                                     |1       |0.17         |0.17   |https://www.lcsc.com/product-detail/C602037.html  |
|C21, C22, C24                                             |Capacitor       |10u             |805                                     |3       |0.18         |0.54   |https://www.lcsc.com/product-detail/C2932476.html |
|C3, C4                                                    |Capacitor       |15p             |402                                     |2       |0.025        |0.05   |https://www.lcsc.com/product-detail/C441742.html  |
|D1, D2                                                    |Diode           |D_Schottky      |D_SOD-123F                              |2       |0.035        |0.07   |https://www.lcsc.com/product-detail/C432153.html  |
|D3, D4, D5                                                |LED             |LED             |402                                     |3       |0.054        |0.162  |https://www.lcsc.com/product-detail/C2980183.html |
|J1                                                        |USB C receptacle|USB_C_Receptacle|USB_C_Receptacle_XKB_U262-16XN-4BVC11   |1       |0.059        |0.059  |https://www.lcsc.com/product-detail/C393939.html  |
|L1                                                        |Inductor        |4.7u            |L_Changjiang_FNR4020S                   |1       |0.082        |0.082  |https://www.lcsc.com/product-detail/C167828.html  |
|R1, R6                                                    |Resistor        |10k             |402                                     |2       |0.0425       |0.085  |https://www.lcsc.com/product-detail/C3020235.html |
|R2, R3                                                    |Resistor        |4.7k            |402                                     |2       |0.0026       |0.0052 |https://www.lcsc.com/product-detail/C25900.html   |
|R4, R5                                                    |Resistor        |5.1k            |402                                     |2       |0.006        |0.012  |https://www.lcsc.com/product-detail/C278598.html  |
|R7                                                        |Resistor        |1k              |402                                     |1       |0.066        |0.066  |https://www.lcsc.com/product-detail/C427241.html  |
|R8                                                        |Resistor        |220             |402                                     |1       |0.002        |0.002  |https://www.lcsc.com/product-detail/C2909336.html |
|R9                                                        |Resistor        |100             |402                                     |1       |0.026        |0.026  |https://www.lcsc.com/product-detail/C427204.html  |
|SW1                                                       |Push button     |SW_Push         |SW_SPST_PTS810                          |1       |0.3425       |0.3425 |https://www.lcsc.com/product-detail/C221895.html  |
|U1                                                        |MCU             |STM32F405RGTx   |LQFP-64_10x10mm_P0.5mm                  |1       |6.01         |6.01   |https://www.lcsc.com/product-detail/C15742.html   |
|U2                                                        |Flash           |W25Q128JVP      |WSON-8-1EP_6x5mm_P1.27mm_EP3.4x4.3mm    |1       |2.82         |2.82   |https://www.lcsc.com/product-detail/C2441427.html |
|U3                                                        |magnetometer    |QMC5883P        |LGA-16_3x3_Pitch0.5mm_QMC5883P          |1       |1.57         |1.57   |https://www.lcsc.com/product-detail/C2847467.html |
|U4                                                        |IMU             |ICM-20602       |LGA-16_3x3mm_P0.5mm_LayoutBorder3x5y    |1       |6.02         |6.02   |https://www.lcsc.com/product-detail/C97633.html   |
|U5                                                        |Pressure Sensor |BMP580          |ST_HLGA-10_2x2mm_P0.5mm_LayoutBorder3x2y|1       |1.21         |1.21   |https://www.lcsc.com/product-detail/C22391138.html|
|U6                                                        |Buck            |AP63205WU       |TSOT-23-6                               |1       |0.43         |0.43   |https://www.lcsc.com/product-detail/C2071056.html |
|U7                                                        |LDO             |TLV75733PDBV    |SOT-23-5                                |1       |0.2          |0.2    |https://www.lcsc.com/product-detail/C485517.html  |
|Y1                                                        |Crystals        |25MHz           |Crystal_SMD_3225-4Pin_3.2x2.5mm         |1       |0.1          |0.1    |https://www.lcsc.com/product-detail/C70582.html   |
|                                                          |                |                |                                        |        |LCSC shipping|9.3    |                                                  |
|                                                          |                |                |                                        |        |PCB Shipping |11.25  |                                                  |
|                                                          |                |                |                                        |        |Total        |45.8309|                                                  |



Made by Keyaan and Ahad

# Licensing
Licensed under the MIT License!