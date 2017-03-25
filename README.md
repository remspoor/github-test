# Electron-Burner
Burn electrons to discharge LiPo batteries to storage level


Depends on these libraries:
---------------------------
- TFT_HX8357
- Encoder

Components used:
----------------
- ILI9481 3.2" 480x320 LCD display (https://www.aliexpress.com/item/Free-shipping-3-2-inch-TFT-LCD-screen-module-Ultra-HD-320X480-for-Arduino-MEGA-2560/32283720984.html)
- IRL3705 Power MOSFET
- ..... (more)


Poormans schematic:
-------------------

`  Balancer cables >----+`
`                       |`
`                       |`
`                      |+|`
`                      | |`
`                      | | 27kOhm`
`                      | |`
`                      |+|`
`                       |`
`                       |`
`                      |+|`
`                      | | 5kOhm`
`                      | |`
`                      | |<----- ADC input`
`                      |+|`
`                       |`
`                       |`
`                      --- GND`

      (Needed 12x)


Output:

                        +-----------------O Positive battery lead
                        |
                        |
                       \ /
                        X  Light bulp
                       / \
                        |
                        |
           100Ohm       |
           -----      |-+
        ---+   +----->|    IRL3705
           -----      |-+
                        |
                        |
                   +----+----+
                   |         |
                  |+|       |+|
                  | |       | | 0.2Ohm/5W
                  | |       | |
  ADC input ----->| |       | |
                  |+|       |+|
                   |         |
                   |         |     +------O Negative battery lead
                   |         |     |
                  ---  GND  ---   --- GND

      (Needed 2x)





