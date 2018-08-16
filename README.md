# NmeaParser

This project demonstrate how to parser NMEA protocol.

## Modules

| Module           | Function                                    |
| ---------------- | ------------------------------------------- |
| `nmea_reader`    | Read NMEA data, contains one NMEA sentence. |
| `nmea_tokenizer` | Split NMEA sentence into `token`s.          |
| `parser`         | Parse nmea `token`s.                        |
| `nav_data`       | Navigation data.                            |

1. Add NMEA data to `nmea_reader` by character.
2. If encounter '\n',  using `nmea_tokenizer` split `nmea_reader`.
3. Parse `nmea_tokenizer` , and store results int `nav_data`.
4. If encounter `GGA` sentence, print `nav_data`.

## Navigation data

#### Latitude

Positive for North, and negative for South.

#### Longitude

Positive for  East, and negative for West.

#### Satellite's PRN and SVID

`PRN` is the satellite's NO. in NMEA. Normally from 1 to 32.

`SVID` is the index in satellite's array.

| SVID range | Constellation type |
| ---------- | ------------------ |
| 1-64       | GPS                |
| 65-96      | GLONASS            |
| 201-232    | Beidou             |



