
SPI Interface
=============

The Serial Peripheral Interface Bus (SPI) bus is a synchronous serial data link.
Devices communicate in master/slave mode where the master device initiates the
data frame. Multiple slave devices are allowed with individual slave select
(chip select) lines.

The SPI bus is said to be a four-wire type serial bus, and is often referred to
as Synchronous Serial Interface (SSI).


A SPI bus with a single master and slave:

```
 +------------------+         +------------------+
 |              SCLK|-------->| SCLK             |
 | SPI          MOSI|-------->| MOSI       SPI   |
 | Master       MISO|<--------| MISO       Slave |
 |              SS  |-------->| SS               |
 +------------------+         +------------------+
```


# Interface

The SPI bus specifies four logic signals:

 * SCLK: serial clock (output from master);
 * MOSI: master output, slave input (output from master);
 * MISO: master input, slave output (output from slave);
 * SS:   slave select (active low, output from master).
