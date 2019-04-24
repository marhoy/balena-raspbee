# balena-raspbee

# Setting up application from scratch

1. Create a new application in Balena
2. Under "Fleet configuration"
   - Enable `RESIN_HOST_CONFIG_enable_uart`
   - Add a new "Custom variable" `RESIN_HOST_CONFIG_dtoverlay` with the value `pi3-miniuart-bt`
3. Add a device to the application
4. Push this repository to the application `balena push <appname>`

# Updating firmware

- Check deconz log for the name of the new firmware. Example `GW update firmware found: /usr/share/deCONZ/firmware/deCONZ_Rpi_0x26330500.bin.GCF`
- Stop deconz container
- Open ssh session in deconz-fw container
- Run `/firmware-update.sh`
