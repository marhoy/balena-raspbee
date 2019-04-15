# balena-raspbee

1. Create a new application in Balena
2. Under "Fleet configuration"
   - Enable `RESIN_HOST_CONFIG_enable_uart`
   - Add a new "Custom variable" `RESIN_HOST_CONFIG_dtoverlay` with the value `pi3-miniuart-bt`
3. Add a device to the application
4. Push this repository to the application `balena push <appname>`
