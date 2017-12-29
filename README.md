# max7219-ticker
An arduino sketch that implements a news ticker on a 8x8 LED matrix driven by a
MAX7219.

## Protocol
Communication with the arduino takes place over a serial connection with a baud
rate of 9600.

The firmware uses a really simple protocol:

1. Send `hi`
2. Wait for a `sup?`
3. Send your null-terminated ticker text.

The device will also indicate that it is waiting for a new text by displaying
three dots.

## License
See the [LICENSE](LICENSE.md) file for license rights and limitations (MIT).
