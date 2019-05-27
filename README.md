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
