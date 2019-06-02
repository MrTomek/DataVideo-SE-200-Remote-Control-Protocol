# DataVideo SE2000 Remote Control Protocol
DataVideo SE-2000 RS-232 Remote Control Protocol



## Remote Control Protocol Communication diagram

### Control Interface
| Name | Data |
|--|--|
| Interface |  RS232 |
| Baud Rate | 115200 |
| Data bits | 8 |
| Parity | None |
| None Stop | 1 |

### Pin Assignment
| PIN | HOST |  | SE-2000 |
|--|--|--|--|
| 2 | Receive A (RX-) | <- | Transmit A (TX-) |
| 3 | Transmit B (TX+) | -> | Receive B (RX+) |
| 5 | Common | --- | Common |

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
  
  
   
   
## Table Status Code

| Byte 1 | Byte 2 | Byte 3 | Byte 4 | Byte 5 | Byte 6 | Byte 7 | Byte 8 | Byte 9 | Byte 10 | Byte 11 | Byte 12 | Byte 13 | Byte 14 | Byte 15 | Byte 16 | Byte 17 | Byte 18 | Byte 19 | Byte 20 | Byte 21 | Byte 22 | Byte 23 | Byte 24 | Byte 25 | Byte 26 | Byte 27 | Byte 28 | Byte 29 | Byte 30 | Byte 31 | Byte 32 | Byte 33 | Byte 34 | Byte 35 | Byte 36 | Byte 37 | Byte 38 | Byte 39 | Byte 40 | Byte 41 |
|--|--|--|--|--|--|--|--|--|--|--|--|--|--|--|--|--|--|--|--|--|--|--| --|--|--|--|--|--|--|--|--|--|--|--|--|--|--|--|--|--|
| Current_User_Number | Input_A | Input_B | PIP_Input | Effect | Speed | Speed_Value_0 | Speed_Value_1  | Speed_Value_2 | Speed_Value_3 | Speed_Value_4 | Mux_Line_A | Mux_Line_B | Bright_Cur | Contrast_Cur | Saturation_Cur | X_Lbl_1 | Y_Lbl_1 | X_Lbl_2 | Y_Lbl_2| Lbl_1_Number | Lbl_2_Number | X_clock | Y_clock | Background_Number | Brightness_Control | Color_Fill | X_PIP | Y_PIP | PIP_Size | Luma_Key_Level | Sys_Format | Inp_3_Mode | Link_Flags | Link_Flags_Ext | Flags_Mixer | Flags_Line_A | Flags_Line_B | Flags_Sources_Position | Flags_DSK | Flags_Lbl |


### Current_User_Number (Byte 1)
Current user number (0…5), number 0 corresponds to the Master User which other the other users settings and adjustments can be linked to

### Input_A, Input_B, PiP_Input  (Byte 2)
Input number currently switched to the multiplexor’s Line A, multiplexor’s Line B and PiP shaper input

### Effect (Byte 3)
Currently set transition effect (curtains): 

	r FB B1 B0 E3 E2 E1 E0 

 - **r** reserved bit
 - **FB** soft border activation flag(0 – off, 1 – on),
 -  **B1, B0**  effect border width, 0… 3
 -  **E3** effect inversion flag(0 – direct, 1 – inverse)
 -  **E2, E1, E0** effect number(0… 5)

### Speed (Byte 4)
Number of the pressed key for speed selection (0… 4);

### Speed_Value_0-4 (Byte 7 - 11)
Predefined speed corresponding to the keys for Speed Selection (4… 64)

### Mux_Line_A, Mux_Line_B (Byte 12 - 13)
The multiplexor’s Line A and Line B status:

	r r r r r M2 M1 M0
 - **r** reserved bits,
 -  **M2, M1, M0** signal source for the Line(000- selected input (Input_A or Input_B), 001- reserved, 010- Color Bars, 011- Color Fill defined by Color_Fill parameter);
 - 
### Bright_Cur  (Byte 14)
Brightness of the last selected source (0x48… 0xb8 with step 8)

### Contrast_Cur  (Byte 15)
 Contrast of the last selected source (0x24… 0x5c with step 4)

### Saturation_Cur (Byte 16)
Color saturation of the last selected source (0x24… 0x5c with step 4)

### X_Lbl_1, X_Lbl_2, X_clock (Byte 17, 19, 23)
 X-coordinate for Logo 1 or Logo 2 or Clock (0… 62 for 1280x720 screen resolution or 0… 102 for 1920x1080 screen resolution)
 
### Y_Lbl_1, Y_Lbl_2, Y_clock  (Byte 18, 20, 24)
Y-coordinate for Logo 1 or Logo 2 or Clock (0… 130 for 1280x720 screen resolution or 0… 110 for 1920x1080 screen resolution)

### Lbl_1_Number (Byte 21)
Logo 1 number (0… 13)

### Lbl_2_Number (Byte 22)
Logo 2 number (0…13)
  
### Background_Number  (Byte 25)
Multiscreen background image number(0…7)

### Brightness_Control (Byte 26)
Keyboard LED brightness factor(0… 1)

### Color_Fill (Byte 27)
Color Fill number(0… 7)

###  X_PiP (Byte 28)
X-coordinate for PiP (0… 70 for 1280x720 screen resolution or 0… 102 for 1920x1080 screen resolution)

### Y_PiP (Byte 29)
Y-coordinate for PiP (0… 77 for 1280x720 screen resolution or 0… 113 for 1920x1080 screen resolution)

### PiP_Size (Byte 30)
PiP size(32… 64) 

### Luma_Key_Level (Byte 31)
Luma Key threshold level(0…255)


### Sys_Format (Byte 32)
Multiscreen resolution (the higher 4 bits) and the output signal system (the lower 4 bits). The following values are valid: 

Mon_1920x1080_i60 = 0 
Mon_1280x720_p60 = 1 

Out_1920x1080_i25 = 0 
Out_1920x1080_i30 = 1 	
Out_1920x1080_i29.95 = 2 
Out_1280x720_p50 = 3 
Out_1280x720_p60 = 4 
Out_1280x720_p59.9 = 5

|Mon|Out| Value (bits4) | Value (bits4) | All |
|--|--|--|--|--|
|1920x1080_i60|1920x1080_i25 | 0 | 0 | 0 |
|1920x1080_i60|Out_1920x1080_i30 | 0 | 1 | 1 |
|1920x1080_i60|Out_1920x1080_i29.95 | 0 | 2 | 2 |
|1920x1080_i60|Out_1280x720_p50 | 0 | 3 | 3 |
|1920x1080_i60|Out_1280x720_p60 | 0 | 4 | 4 |
|1920x1080_i60|Out_1280x720_p59.9 | 0 | 5 | 5 |
|--|--|--|--|--|
|1280x720_p60|1920x1080_i25 | 1 | 0 | 16 |
|1280x720_p60|Out_1920x1080_i30 | 1 | 1 | 17 |
|1280x720_p60|Out_1920x1080_i29.95 | 1 | 2 | 18 |
|1280x720_p60|Out_1280x720_p50 | 1 | 3 | 19 |
|1280x720_p60|Out_1280x720_p60 | 1 | 4 | 20 |
|1280x720_p60|Out_1280x720_p59.9 | 1 | 5 | 21 |


### Inp_3_Mode (Byte 33)
The current input 3 mode, 0 – SDI, 1 – DVI;

### Link_Flags (Byte 34)
Master user settings link flags, it may be unlinked(value 0) or linked(value1) to the corresponding basic parameter: 
 - **bit 7:** input 0 settings link flag (brightness, contrast, saturation)
 - **bit 6:** input 1 settings link flag (brightness, contrast, saturation)
 - **bit 5:** input 2 settings link flag (brightness, contrast, saturation)
 - **bit 4:** input 3 settings link flag (brightness, contrast, saturation)
 - **bit 3:** input 4 settings link flag (brightness, contrast, saturation)
 - **bit 2:** position and numbers of the Logo 1, Logo 2 and Clock position link flag
 - **bit 1** PiP position and size link flag
 - **bit 0** input 3 mode link flag

### Link_Flags_Ext (Byte 35)
Master User settings extended flags, it may be unlinked (value 0) or linked (value 1) to the corresponding basic parameter: 
- **bit 7:** output signal system link flag
- **bit 6:** multiscreen resolution link flag
- **bit 5:** Luma Key threshold level link flag
- **bits 4… 0:** reserved, ignore
- 
### Flags_Mixer (Byte 36)
Switching flags (mixing): 
 - **bit 7:** Line connected to Program output (Main Source), 0 – LineA, 1 – LineB, 
- **bit 6:**  reserved, ignore
- **bit 5:**  reserved, ignore
- **bit 4:**  switch mode, 0 – mixing

### Flags_Line_A, Flags_Line_B (Byte 37-38)
Frame freeze flags of Line A and Line B: 
 - **bit 7:** 0 - Frame freeze off, 1 - Frame freeze on 
 - **bits 6… 0:** reserved, ignore
 - 
### Flags_Sources_Position (Byte 39)
 Selection Key inversion flags and switcher’s T-bar mode flag: 
 - **bit 7:** 0 – keyboard’s source Selection Keys are arranged in direct manner (Source 1 is on the left), 1 – inverse manner (Bar is on the left)
 -  **bit 6:** 0 – T-bar is active only while moving upwards, 1 – T-bar is active while moving both upwards and downwards 
 - **bits 5… 0:** reserved, ignore
 - 
### Flags_DSK (Byte 40)
PiP and Luma Key out flags: 
- **bit 7… 6:** reserved, ignore
- **bit 5:** 1 – Luma Key is output onto Preview channel, 0 – not
- **bit 4:** 1 – Luma Key is output onto Program channel, 0 – not
- **bit 3:** 1 – PiP is output onto Preview channel, 0 – not
- **bit 2:** 1 – PiP is output onto Program channel, 0 – not
- **bits 1… 0:** – reserved, ignore


### Flags_Lbl (Byte 41)
Logo and Clock activation flags: 

- **bit 7:** 1 – Logo 1 is output onto Program channel, 0 – not, 
- **bit 6:** 1 – Logo 2 is output onto Program channel, 0 – not, 
- **bit 5:** 1 – Logo 1 is output onto Preview channel, 0 – not, 
- **bit 4:** 1 – Logo 2 is output onto Preview channel, 0 – not, 
- **bit 3:** Clock activation instead of Logo 2 (0- Logo 2, 1- Clock), 
- **bits 2… 0:** reserved, ignore;
- 
1.26. COM = 0xA0 – copy and write setting parameters Common_Settings (Section 2) from the device’s EEPROM into the device’s volatile memory. ARG = 0. Device replies with LEN = 0, ANSW is not available. 

1.27. COM = 0xA0 – device soft reset. ARG = 0. Device replies with LEN = 0, ANSW is not available. The device executes soft reset and it completely reboots (similar to the power recycle). It is impossible to establish a connection with the device for around 8 seconds.
