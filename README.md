# 1 Button MIDI Controller

These demos distill MIDI WiFi to its simplest form. This makes understanding
how the programs work much easier. One ESP8266 or ESP32 WiFi board with a
button is all that is needed. No DIN connectors, UARTs, or USB are needed.

The demos were tested on an ESP8266 NodeMCU 1.0 and an ESP32 development board.
Both boards include a button.  If the ESP board you use does not have button,
you can add one to any available GPIO pin.

Additional software is required on Macs, Windows, and Linux computers to speak
MIDI multicast and RTP MIDI. I highly recommend reading the TouchDAW
documentation. The same procedures to get TouchDAW connected, are required to
make these demos to work. UDP multicast is much easier to setup but RTP MIDI may
perform better on busy WiFi networks.

http://www.humatic.de/htools/touchdaw/drivers.htm

http://www.humatic.de/htools/touchdaw/man_midi.htm

midi1button/

    The midi1button demo uses Multicast UDP to send MIDI messages. Three
    options are included. Option 1 sends Note On/Off when the button is
    pressed/released. Option 2 sends Change Control Sustain On/Off when the
    button is pressed/released. This could be used with one or more foot
    pedals.  Option 3 sends All Notes Off on all channels when the button is
    pressed.

midi1buttonrtp/

    The midi1buttonrtp demo uses RTP MIDI (also known as Apple MIDI) to send
    MIDI messages. The demo has the same options as the first demo but uses RTP
    MIDI instead of UDP multicast.
