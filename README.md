# cambridge_audio_cxa
Home Assistant Custom Component for controlling Cambridge Audio CXA amplifiers

Create a directory called <b>cambridge_cxa</b> under the custom_components directory, and save the files from this repo in there.

Then, add the following to your configuration.yaml file:

```
media_player:
  - platform: cambridge_cxa
    host: <IP address of raspberry pi that has the USB to serial connection to the amp>
    username: <SSH username to login to the raspberry pi>
    type: CXA81 or XCA61
    name: <Optional value, to override default name: Cambridge Audio CXA>
    slave: <Optional value, if you have a CXN, enter its IP address here, so you can control the CXA's volume through the CXN>
```

Make sure you copy the SSH key from your Home Assistance instance to the raspberry pi, so you can issue commands over SSH without providing your password.

You can use the <b>ssh-keygen</b> and <b>ssh-copy-id</b> commands for that.

Reboot Home Assistant, and see you have a new media_player entity for youtr CXA.
