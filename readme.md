## ST LoRa
Projects based on a pair of STM P-Nucleo-LRWAN1 kits containing an STM32L073 and an SX1272MB2xAS embed shield.

### STM32CubeExpansion_LRWAN_V2.1.0
Initial project is just playing with the SubGHz_Phy_PingPong example for STM32L073RZ.
Project builds with IAR WARM 8.40.2
Note: Watch dog is not handled, so don't enable the HW WD in option bits!
Project is set for US 915 band.

#### To DO
- blink the user LED to indicate TX/RX (for range testing)
- put a counter in the RTC IRQ so debugger can see loop count. (what is the IRQ/loop rate anyway?)
- build battery/non-battery versions.
    - enable debug in LP/stop mode in HAL_MspInit()
    - build in non low-power (LOW_POWER_DISABLE) and measure current. (ie for nod attached to system)
- investigate PROBE_PINS_ENABLED and PROBE1 and PROBE2
- periodically dump RTC to serial.
