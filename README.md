# wifi-page
WiFi enabled sidecar board enabling embedded devices to communicate with the cloud

## Known Issues in v1r1

- If you aren't careful when scratching the trace to switch the power path, there could be backfeed. We experienced the LDO drawing too much current despite the other pins being bridged, and the voltage on the power rail dropped to ~1V.
- There is no pull-down resistor on IO46, which is one of the strapping pins for flashing over UART using the joint download mode. We fixed this temporarily by tacking a wire between IO46 and GND.
