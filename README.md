# DataVideo-SE-200-Remote-Control-Protocol
DataVideo SE-2000 RS-232 Remote Control Protocol

## Table Command Type


| No. | COM(Hex) | ARG (Hex) | Description | 
|--|--|--|--|
| 1 | **00** | 00 | Sub source: Set SDI input port 1 |
|  |  | 01 | Sub source: Set SDI input port 2 |
|  |  | 02 | Sub source: Set SDI input port 3 |
|  |  | 03 | Sub source: Set SDI input port 4 |
|  |  | 04 | Sub source: Set SDI input port 5 |
| 2 | **01** | 00 | Sub source: Set Black Screen |
| 3 | **02** | 00 | Sub source: Set Colour Bar |
| 4 | **03** | 00 | Main source: Set SDI input port 1 | 
|  |  | 01 | Main source: Set SDI input port 2 | 
|  |  | 02 | Main source: Set SDI input port 3 | 
|  |  | 03 | Main source: Set SDI input port 4 | 
|  |  | 04 | Main source: Set SDI input port 5 | 
| 5 | **04** | 00 | Main source: Set Black Screen | 
| 6 | **05** | 00 | Main source: Set Colour Bar | 
| 7 | **10** | 00 |  Logo 1 turn off | 
|  |  | 01 | Logo 1 turn on | 
| 8 | **11** | 00 | Logo 2 and Clock turn off | 
|  |  | 01 | Logo 2 turn on | 
|  |  | 02 | Clock turn on | 
| 9 | **20** | 00 | Auto function : Set Speed as level 1 | 
|  |  | 01 | Auto function : Set Speed as level 2 | 
|  |  | 02 | Auto function : Set Speed as level 3 | 
|  |  | 03 | Auto function : Set Speed as level 4 | 
|  |  | 04 | Auto function : Set Speed as level 5 | 
| 10 | **30** | 00 | Wipe Effect Type 1 |
|  |  | 01 | Wipe Effect Type 2 | 
|  |  | 02 | Wipe Effect Type 3 | 
|  |  | 03 | Wipe Effect Type 4 | 
|  |  | 04 | Wipe Effect Type 5 | 
|  |  | 05 | Wipe Effect Type 6 | 
|  |  | 08 | Wipe Effect Type 1 of Inversion | 
|  |  | 09 | Wipe Effect Type 2 of Inversion | 
|  |  | 0A | Wipe Effect Type 3 of Inversion | 
|  |  | 0B | Wipe Effect Type 4 of Inversion | 
|  |  | 0C | Wipe Effect Type 5 of Inversion | 
|  |  | 0D | Wipe Effect Type 6 of Inversion | 
| 11 | **31** | 00 | Effect hard border | 
|  |  | 01 | Effect soft border | 
| 12 | **32** | 00 | Mix function | 
|  |  | 01 | Wipe function | 
| 13 | **40** | 00 | Cut function | 
| 14 | **41** | 00 | Auto function | 
| 15 | **50**  | 00 | PIP source: Set SDI input port 1 | 
|  |  | 01 | PIP source: Set SDI input port 2 | 
|  |  | 02 | PIP source: Set SDI input port 3 |
|  |  | 03 | PIP source: Set SDI input port 4 |
|  |  | 04 | PIP source: Set SDI input port 5 |
| 16 | **51** | 00 | PIP display on Sub source |
|  |  | 01 | PIP turn off on Sub source |
| 17 | **52** | 00 | PIP display on Main source |
|  |  | 01 | PIP turn off on Main source |
| 18 | **61** | 00 | Luma disable on Sub source |
|  |  | 01 | Luma enable on Sub source |
| 19 | **62** | 00 | Luma disable on Main source |
|  |  | 01 | Luma enable on Main source |
| 20 | **70** | 00 | Frame Freeze turn off |
|  |  | 01 | Frame Freeze turn on |
| 21 | **80** | 00 | Frame System time read |
| 22 | **81** | Hours(BCD) | System time of Hour adjustment |
| 23 | **82** | Minutes(BCD) | System time of Minute adjustment |
| 24 | **83** | Second(BCD) | System time of Second adjustment |
| 25 | **90** | 00 | Get device status |
