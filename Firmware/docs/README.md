<!DOCTYPE html>
<html>
<head>
<BIG>Modd OSD Register Set </BIG>
</head>
<body style="background-color:powderblue;">
<!-- ---------------------------------------------------------- -->
<a name="TOP"></a> 

<BR> proposed, first draft.<BR><BR>

implemented(mostly).
<table style="width:100%">
  <tr>
    <th style="width:5%">NUM</th>
    <th style="width:5%">Reg</th>
    <th style="width:5%">Default</th>   
    <th style="width:10%">MAX7456 Compatibility</th>
    <th>Name</th>
  </tr>
  <tr>
    <td>0x00</td> <td><a href=#VM0>VM0</a></td> <td>0</td>  <td>Partial/New</td> <td>Video Mode 0</td>
  </tr>
  <tr>
    <td>0x01</td> <td><a href=#VM1>VM1</a></td> <td>0</td>  <td>No</td> <td>Video Mode 1</td>
  </tr>
  <tr>
    <td>0x02</td> <td><a href=#HOS>HOS</a></td> <td>0</td>  <td>Supported</td> <td>Horizontal Offset</td>
  </tr>  
  <tr>
    <td>0x03</td> <td><a href=#VOS>VOS</a></td> <td>0</td>  <td>Supported</td> <td>Vertical Offset</td>
  </tr>  
  <tr>
    <td>0x04</td> <td><a href=#DMM>DMM</a></td> <td></td>  <td>Partial</td> <td>Display Memory Mode</td>
  </tr>  
  <tr>
    <td>0x05</td> <td><a href=#DMAH>DMAH</a></td> <td></td>  <td>Extended</td> <td>Display Memory Address High</td>
  </tr>  
  <tr>
    <td>0x06</td> <td><a href=#DMAL>DMAL</a></td> <td></td>  <td>Supported</td> <td>Display Memory Address Low</td>
  </tr>  
  <tr>
    <td>0x07</td> <td><a href=#DMDI>DMDI</a></td> <td></td>  <td>Supported</td> <td>Display Memory Data In</td>
  </tr>  
  <tr><td>0x08</td> <td>CMM</td> <td>0</td>  <td>Ignored</td> <td>Character Memory Mode</td>
  </tr>  
  <tr><td>0x09</td> <td>CMAH</td> <td>0</td>  <td>Ignored</td> <td>Character Memory Address High</td>
  </tr>  
  <tr><td>0x0A</td> <td>CMAL</td> <td>0</td>  <td>Ignored</td> <td>Character Memory Address Low</td>
  </tr>  
  <tr><td>0x0B</td> <td>CMDI</td> <td>0</td>  <td>Ignored</td> <td>Character Memory Data In</td>
  </tr>  

  <tr><td>0x0C</td> <td><a href=#OSDM>OSDM</a></td> <td></td>  <td>Partial</td> <td>OSD Insertion Mux</td></tr>  
  <tr><td>0x0D</td> <td><a href=#VM2>VM2</a></td>   <td></td>  <td>New</td> <td>Video Mode 2</td></tr>  


  <tr>
    <td>0x10-<BR>0x1F</td> <td>RBx</td> <td>0</td>  <td>Ignored</td> <td>Row 0-15 Brightness</td>
  </tr>  


  <tr><td>0x30</td> <td><a href=#FBS>FBS</a></td> <td>255</td>  <td>New</td> <td>Font Bank Select</td>  </tr>  
  <tr><td>0x31</td> <td><a href=#FNTS>FNTS</a></td> <td>255</td>  <td>New</td> <td>Font Set</td>  </tr>  

  <tr><td>0x34</td> <td><a href=#MXLS>MXLS</a></td> <td>255</td>  <td>New</td> <td>Mixer Line Select</td>  </tr>  
  <tr><td>0x35</td> <td><a href=#MXCC>MXCC</a></td> <td>255</td>  <td>New</td> <td>Mixer Line Color 3 / Color 1</td>  </tr>  
  <tr><td>0x36</td> <td><a href=#MXTC>MXTC</a></td> <td>255</td>  <td>New</td> <td>Mixer Line Transparent / Color 2</td>  </tr>  
  <tr><td>0x37</td> <td><a href=#MXM>MXM</a></td> <td>255</td>  <td>New</td> <td>Mixer Mode</td>  </tr>  


  <tr><td>0x38</td> <td><a href=#SOS>SOS</a></td> <td>0</td>  <td>New</td> <td>Servo Select</td>  </tr>  
  <tr><td>0x39</td> <td><a href=#SOV>SOV</a></td> <td>128</td>  <td>New</td> <td>Servo Value</td>  </tr>  
  <tr><td>0x3A</td> <td><a href=#SOW>SOW</a></td> <td>200</td>  <td>New</td> <td>Servo Width</td>  </tr>  
  <tr><td>0x3B</td> <td><a href=#SOT>SOT</a></td> <td>128</td>  <td>New</td> <td>Servo Trim</td>  </tr>  


  <tr><td>0x3E</td> <td><a href=#DBUG>DBUG</a></td> <td>0</td>  <td>New</td> <td>Debug Register</td>  </tr>  
  <tr><td>0x3F</td> <td><a href=#EXE>EXE</a></td>  <td>0</td>  <td>New</td> <td>Execute Buffer Register</td>  </tr>  
  <tr><td>0x40-0x7F</td> <td><a href=#BUFF>BUFF</a></td> <td></td>  <td>New</td> <td>Command Buffer/Font Update Buffer
<BR><a href=#GFXCMD>Graphics Commands</a><BR><a href=#GENCMD>General Commands</a><BR></td></tr>

  <tr><td>0x6C</td> <td></td> <td></td>  <td>Repurposed</td> <td>OSD Black Level</td></tr>  
  <tr><td>0xAx</td> <td></td> <td></td>  <td></td> <td>Read Status</td></tr>  
  <tr><td>0xBx</td> <td></td> <td></td>  <td>Unsupported</td> <td>Display Memory Data Out</td></tr>  
  <tr><td>0xCx</td> <td></td> <td></td>  <td>Unsupported</td> <td>Character Memory Data Out</td></tr>
</table>
<BR><BR><BR>
Future
<table style="width:100%">
  <tr>
    <th style="width:5%">NUM</th>
    <th style="width:5%">Reg</th>
    <th style="width:5%">Default</th>   
    <th style="width:10%">MAX7456 Compatibility</th>
    <th>Name</th>
  </tr>
  <tr><td>tbd</td> <td>GYX</td> <td></td>  <td>tbd</td> <td>Gyro X Value</td></tr>  
  <tr><td>tbd</td> <td>GYY</td> <td></td>  <td>tbd</td> <td>Gyro Y Value</td></tr>  
  <tr><td>tbd</td> <td>BARO</td> <td></td>  <td>tbd</td> <td>Barometer Value</td></tr>  
  <tr><td>tbd</td> <td>ARTH</td> <td>0</td>  <td>tbd</td> <td>Graphic Artificial Horizon Control</td>  </tr>  
  <tr><td>tbd</td> <td>GHC</td>  <td>0</td>  <td>tbd</td> <td>Graphic Height Control</td>  </tr>  


  <tr><td>tbd</td> <td><a href=#SHS>SHIS</a></td> <td>255</td>  <td>tbd</td> <td>Shifter Select</td>  </tr>  
  <tr><td>tbd</td> <td><a href=#SHIM>SHIM</a></td> <td>255</td>  <td>tbd</td> <td>Shifter Mode</td>  </tr>  
  <tr><td>tbd</td> <td><a href=#SHIZ>SHIZ</a></td> <td>255</td>  <td>tbd</td> <td>Shifter Size</td>  </tr>  
  <tr><td>tbd</td> <td><a href=#SHIP>SHIP</a></td> <td>255</td>  <td>tbd</td> <td>Shifter Position</td>  </tr>  
  <tr><td>tbd</td> <td><a href=#SHIV>SHIV</a></td> <td>255</td>  <td>tbd</td> <td>Shifter Value</td>  </tr>  


</table>

<!-- ---------------------------------------------------------- -->
<BR><a name="VM0"></a><a href=#TOP>index</a><BR> 
<table style="width:100%">  <th style="width:15%"><b>VM0</b></th> <th style="width:10%"><b>0x00</b></th> <th><b>Video Mode 0</b></th> </table>
<table style="width:100%">
  <tr>
    <th style="width:7%">BIT</th>
    <th style="width:8%">Default</th>   
    <th style="width:10%">Compat</th>
    <th>Function</th>
  </tr>
  <tr><td>7</td>    <td>0</td>   <td>New</td>     <td>MAX7456 Compatability Mode 0=ON 1=OFF.  Sets the display width to 30 chars among other things.</td></tr>
  <tr><td>6</td>    <td>0</td>   <td>Partial</td> <td>Video Standard Select 0=NTSC 1=PAL  (*)Self generated video always NTSC.</td></tr>
  <tr><td>5,4</td>  <td>00</td>  <td>Full</td>    <td>Sync Select Mode 0x=AUTO 10=EXTERNAL 11=GENERATED </td></tr>
  <tr><td>3</td>    <td>0</td>   <td>Full</td>    <td>Enable Display of OSD Image 0=OFF 1=ON</td></tr>
  <tr><td>2</td>    <td>0</td>   <td>No</td>      <td>Vertical Synchronization of On-Screen Data</td></tr>
  <tr><td>1</td>    <td>0</td>   <td>Partial</td> <td>Software Reset Bit, Only clears screen and sets mixer variables to defaults</td></tr>
  <tr><td>0</td>    <td>0</td>   <td>No</td>      <td>Video Buffer Enable, 0 = Enable, 1 = Disable (VOUT is high impedance)  </td></tr> 
</table>
<!-- ---------------------------------------------------------- -->
<BR><a name="VM1"></a><a href=#TOP>index</a><BR> 
<table style="width:100%">  <th style="width:15%"><b>VM1</b></th> <th style="width:10%"><b>0x01</b></th> <th><b>Video Mode 1</b></th> </table>
<table style="width:100%"><td>See Mixer variables for similar functionality. </td></table>
<table style="width:100%">
  <tr>
    <th style="width:7%">BIT</th>
    <th style="width:8%">Default</th>   
    <th style="width:10%">Compat</th>
    <th>Function</th>
  </tr>
  <tr><td>7</td>      <td>0</td>    <td>No</td>      <td>Background Mode</td></tr>
  <tr><td>6,5,4</td>  <td>100</td>  <td>No</td>      <td>Background Mode Brightness</td></tr>
  <tr><td>3,2</td>    <td>01</td>   <td>No</td>      <td>Blinking Time</td></tr>
  <tr><td>1,0</td>    <td>11</td>   <td>No</td>      <td>Blinking Duty Cycle</td></tr>
</table>


<!-- ---------------------------------------------------------- -->
<BR><a name="HOS"></a><a href=#TOP>index</a><BR> 
<table style="width:100%">  <th style="width:15%"><b>HOS</b></th> <th style="width:10%"><b>0x02</b></th> <th><b>Horizontal Offset Register</b></th> </table>
<table style="width:100%">
  <tr>
    <th style="width:7%">BIT</th>
    <th style="width:8%">Default</th>   
    <th style="width:10%">Compat</th>
    <th>Function</th>
  </tr>
  <tr><td>7,6</td>  <td>00</td>  <td></td> <td>Don’t Care</td></tr>
  <tr><td>5-0</td>  <td>100000</td>  <td>Full</td> <td>Horizontal Position Offset <BR>00 0000 = Farthest left<BR>11 1111 = Farthest right </td></tr>
</table>


<!-- ---------------------------------------------------------- -->
<BR><a name="VOS"></a><a href=#TOP>index</a><BR> 
<table style="width:100%">  <th style="width:15%"><b>VOS</b></th> <th style="width:10%"><b>0x03</b></th> <th><b>Vertical Offset Register</b></th> </table>
<table style="width:100%">
  <tr>
    <th style="width:7%">BIT</th>
    <th style="width:8%">Default</th>   
    <th style="width:10%">Compat</th>
    <th>Function</th>
  </tr>
  <tr><td>7,6,5</td>  <td>000</td>  <td></td> <td>Don’t Care</td></tr>
  <tr><td>4-0</td>  <td>10000</td>  <td>Full</td> <td>Vertical Position Offset <BR>0 0000 = Farthest Up<BR>1 1111 = Farthest Down </td></tr>
</table>


<!-- ---------------------------------------------------------- -->
<BR><a name="DMM"></a><a href=#TOP>index</a><BR> 
<table style="width:100%">  <th style="width:15%"><b>DMM</b></th> <th style="width:10%"><b>0x04</b></th> <th><b>Display Memory Mode</b></th> </table>
<table style="width:100%">
  <tr>
    <th style="width:7%">BIT</th>
    <th style="width:8%">Default</th>   
    <th style="width:10%">Compat</th>
    <th>Function</th>
  </tr>
  <tr><td>7</td>  <td>000</td>  <td></td> <td>Don’t Care</td></tr>
  <tr><td>6</td>  <td>0</td>  <td>Compatible</td> <td>Operation Mode Selection  <BR>0 = 16-bit operation mode  <BR>1 = 8-bit operation mode 
  <BR>Attribute bytes not supported, when in 16 bit mode attribute byte is discarded.</td></tr>
  <tr><td>5</td>  <td>0</td>  <td>No</td> <td>Local Background Control Bit</td></tr>
  <tr><td>4</td>  <td>0</td>  <td>No</td> <td>Blink Bit, BLK</td></tr>
  <tr><td>3</td>  <td>0</td>  <td>No</td> <td>Invert Bit, INV</td></tr>
  <tr><td>2</td>  <td>0</td>  <td>Full</td> <td>Clear Display Memory  1 = Clear display</td></tr>
  <tr><td>1</td>  <td>0</td>  <td>No</td> <td>Vertical Sync Clear</td></tr>
  <tr><td>0</td>  <td>0</td>  <td>Full</td> <td>Auto-Increment Mode 0 = Disabled 1 = Enabled</td></tr>
</table>


<!-- ---------------------------------------------------------- -->
<BR><a name="DMAH"></a><a href=#TOP>index</a><BR> 
<table style="width:100%">  <th style="width:15%"><b>DMAH</b></th> <th style="width:10%"><b>0x05</b></th> <th><b>Display Memory Address High Register</b></th> </table>
<table style="width:100%">
  <tr>
    <th style="width:7%">BIT</th>
    <th style="width:8%">Default</th>   
    <th style="width:10%">Compat</th>
    <th>Function</th>
  </tr>
  <tr><td>7</td>  <td></td>  <td></td> <td>Don’t Care</td></tr>
  <tr><td>6-4</td>  <td>111</td>  <td>New</td> <td>Font Output Select (Note:Layout can be modified using <a href=#FBS>FBS</a> and <a href=#FNTS>FNTS</a>.) 
   <BR> 000 = Betaflight Default 
   <BR> 001 = Betaflight Vision 
   <BR> 010 = Betaflight Clarity 
   <BR> 011 = Betaflight Bold 
   <BR> 100 = Betaflight Digital 
   <BR> 101 = Betaflight Extra Large 
   <BR> 110 = Ansi Thin Upper/Lower Case Font 
   <BR> 111 = Ansi Upper/Lower Case Font </td></tr>
  <tr><td>3-2</td>  <td></td>  <td></td> <td>Don’t Care</td></tr>
  <tr><td>1</td>  <td>0</td>  <td>Repurposed</td> <td>Display Memory Address Bit 9<BR>Only needed when running in interlace mode (<a href=#VM2>VM2</a> Bit7)  
    <BR>MAX7456 used it to select attribute byte write. (attribute bytes not supported) </td></tr>
  <tr><td>0</td>  <td>0</td>  <td>Full</td> <td>Display Memory Address Bit 8</td></tr>
</table>


<!-- ---------------------------------------------------------- -->
<BR><a name="DMAL"></a><a href=#TOP>index</a><BR> 
<table style="width:100%">  <th style="width:15%"><b>DMAL</b></th> <th style="width:10%"><b>0x06</b></th> <th><b>Display Memory Address Low Register</b></th> </table>
<table style="width:100%">
  <tr>
    <th style="width:7%">BIT</th>
    <th style="width:8%">Default</th>   
    <th style="width:10%">Compat</th>
    <th>Function</th>
  </tr>
  <tr><td>7-0</td>  <td>0x00</td>  <td>Full</td> <td>Display Memory Address Bits 7–0<BR>The lower 8 bits of the display memory address</td></tr>
</table>


<!-- ---------------------------------------------------------- -->
<BR><a name="DMDI"></a><a href=#TOP>index</a><BR> 
<table style="width:100%">  <th style="width:15%"><b>DMDI</b></th> <th style="width:10%"><b>0x07</b></th> <th><b>Display Memory Data In Register</b></th> </table>
<table style="width:100%">
  <tr>
    <th style="width:7%">BIT</th>
    <th style="width:8%">Default</th>   
    <th style="width:10%">Compat</th>
    <th>Function</th>
  </tr>
  <tr><td>7-0</td>  <td>0x00</td>  <td>Full</td> <td>Writes a character to display memory. 
    <BR>The address is determined by ((DMAH & 3)<<8) | DMAL.  
    <BR>This value may be auto incremented if <a href=#DMM>DMM</a> bit 0 is set.</td></tr>
</table>
<!-- ---------------------------------------------------------- -->
<BR><a name="OSDM"></a><a href=#TOP>index</a><BR> 
<table style="width:100%">  <th style="width:15%"><b>OSDM</b></th> <th style="width:10%"><b>0x0</b></th> <th><b>OSD Insertion Mux Register</b></th> </table>
<table style="width:100%">
  <tr>
    <th style="width:7%">BIT</th>
    <th style="width:8%">Default</th>   
    <th style="width:10%">Compat</th>
    <th>Function</th>
  </tr>
    <tr><td>7-6</td>  <td>00</td>     <td></td>        <td>Don’t Care</td></tr>
    <tr><td>5-3</td>  <td>011</td>    <td>Partial</td>     <td>If value is > 4 then a smoothing cap added to OSD signal.</td></tr>
    <tr><td>2-0</td>  <td>011</td>    <td>Ignored</td>     <td>Don’t Care</td></tr>
</table>
<!-- ---------------------------------------------------------- -->
<BR><a name="VM2"></a><a href=#TOP>index</a><BR> 
<table style="width:100%">  <th style="width:15%"><b>VM2</b></th> <th style="width:10%"><b>0x0</b></th> <th><b>Video Mode 2</b></th> </table>
<table style="width:100%">
  <tr>
    <th style="width:7%">BIT</th>
    <th style="width:8%">Default</th>   
    <th style="width:10%">Compat</th>
    <th>Function</th>
  </tr>
    <tr><td>7</td>    <td>0</td>     <td>New</td>  <td>Interlace Mode Select 0=OFF 1=ON</td></tr>
    <tr><td>6-4</td>  <td></td>      <td></td>     <td>Don’t Care</td></tr>
    <tr><td>3-0</td>  <td>0000</td>  <td>New</td>  <td>Selects the start line to display, allows primitive scrolling.  
          <BR> Value clipped to line 32, max value depends on NTSC/PAL and interlace mode.</td></tr>
</table>
<!-- ---------------------------------------------------------- -->
<!-- ---------------------------------------------------------- -->
<!-- ---------------------------------------------------------- -->
<BR> 
<a name="SHIS"></a>
<a name="SHIV"></a>
<a name="SHIP"></a>
<a name="SHIM"></a>
<a name="SHIZ"></a><a href=#TOP>index</a><BR>
Shifter registers under development.  
The idea is to make an easy way to display realtime data in graphical form.
For instance you could periodically write the gyro angle to see how this value changes during your flight.
<BR><BR>
<!-- ---------------------------------------------------------- -->
<!-- ---------------------------------------------------------- -->
<!-- ---------------------------------------------------------- -->
<BR><a name="FBS"></a><a href=#TOP>index</a><BR> 
<table style="width:100%">  <th style="width:15%"><b>FBS</b></th> <th style="width:10%"><b>0x30</b></th> <th><b>Font Bank Select</b></th> </table>
<table style="width:100%"><td>Fonts are split into into 32 character banks.  8 banks are combined into a 256 char fontset. 
 Fontsets are selected in <a href=#DMAH>DMAH</a> bits 4-6. If DHAH[6:4]=0 then banks 0-7 are selected. If DHAH[6:4]=1 then banks 8-15 are selected...<BR> 
This register selects a individual font bank 0-63.  Its value can then be modified using the FNTS register.
</td></table>
<table style="width:100%"> <tr><th style="width:7%">BIT</th><th style="width:8%">Default</th><th style="width:10%">Compat</th><th>Function</th></tr>

  <tr><td>7-6</td>  <td>00</td>      <td></td>     <td>Don’t Care</td></tr>
  <tr><td>5-0</td>  <td>000000</td>  <td>New</td> <td>Selects a font bank (0-63).<br></td></tr>
</table>
<!-- ---------------------------------------------------------- -->
<BR><a name="FNTS"></a><a href=#TOP>index</a><BR> 
<table style="width:100%">  <th style="width:15%"><b>FNTS</b></th> <th style="width:10%"><b>0x31</b></th> <th><b>Font Bank Set</b></th> </table>
<table style="width:100%"><td>Font banks are stored on a single 2K FLASH rom page.  Flash rom is shared with code.  Fonts are stored in the last 96K-88K of flash memory aliased to a 2K boundry.  (Note: there is a 64K flash rom part which can be used with a single font bank, for 11 cents less, but is not officially supported)
</td></table>
<table style="width:100%"> <tr><th style="width:7%">BIT</th><th style="width:8%">Default</th><th style="width:10%">Compat</th><th>Function</th></tr>

  <tr><td>7-2</td>  <td>000000</td>  <td>New</td> <td>Sets the font bank, selected in FBS register, to a specific 2K FLASH rom page.<br></td></tr>
  <tr><td>0-1</td>  <td>00</td>      <td>New</td> <td>Offset 00 = 0, 01 = +4, 10 = -4, 11 = -8 lines</td></tr>
</table>
<!-- ---------------------------------------------------------- -->
<BR><a name="MXLS"></a><a href=#TOP>index</a><BR> 
<table style="width:100%">  <th style="width:15%"><b>MXLS</b></th> <th style="width:10%"><b>0x34</b></th> <th><b>Mixer Line Select</b></th> </table>
<table style="width:100%">
  <tr>
    <th style="width:7%">BIT</th>
    <th style="width:8%">Default</th>   
    <th style="width:10%">Compat</th>
    <th>Function</th>
  </tr>
  <tr><td>7</td>  <td>0</td>  <td>New</td>  <td>Selects all layer1 (gfx) lines.<br></td></tr>
  <tr><td>6</td>  <td>0</td>  <td>New</td>  <td>Selects all layer0 (text) lines.<br></td></tr>
  <tr><td>5</td>  <td>0</td>  <td>New</td>  <td>Selects the layer for bits 4-0.<br></td></tr>
  <tr><td>4-0</td>  <td>00000</td>  <td>New</td> 
    <td>Selects an individual line (0-31).<br></td></tr>
</table>
<!-- ---------------------------------------------------------- -->
<BR><a name="MXCC"></a><a href=#TOP>index</a><BR> 
<table style="width:100%">  <th style="width:15%"><b>MXCC</b></th> <th style="width:10%"><b>0x35</b></th> <th><b>Mixer Color #3 / Color #1</b></th> </table>
<table style="width:100%">
  <tr>
    <th style="width:7%">BIT</th>
    <th style="width:8%">Default</th>   
    <th style="width:10%">Compat</th>
    <th>Function</th>
  </tr>
  <tr><td>7-4</td>  <td>0000</td>  <td>New</td> 
    <td>Selects color #3 (lite) for the lines selected in MXLS register.
      <BR>0 = Transparent<BR>1 = Black<BR>2 = <BR>3 = <BR>4 = Dark Grey <BR>5 = <BR>6 = 
      <BR>7 = Med Grey <BR>8 = <BR>9 = <BR>10 = Lite Grey <BR>11 = <BR>12-16 = White <br></td></tr>

  <tr><td>3-0</td>  <td>0000</td>  <td>New</td> 
    <td>Selects color #1 (dark) for the lines selected in MXLS register.
      <BR>0 = Transparent<BR>1 = Black<BR>2 = <BR>3 = <BR>4 = Dark Grey <BR>5 = <BR>6 = 
      <BR>7 = Med Grey <BR>8 = <BR>9 = <BR>10 = Lite Grey <BR>11 = <BR>12-16 = White <br></td></tr>
</table>
<!-- ---------------------------------------------------------- -->
<BR><a name="MXTC"></a><a href=#TOP>index</a><BR> 
<table style="width:100%">  <th style="width:15%"><b>MXTC</b></th> <th style="width:10%"><b>0x36</b></th> <th><b>Mixer Mix Transparent/Color #2</b></th> </table>
<table style="width:100%">
  <tr>
    <th style="width:7%">BIT</th>
    <th style="width:8%">Default</th>   
    <th style="width:10%">Compat</th>
    <th>Function</th>
  </tr>
  <tr><td>7-4</td>  <td>0000</td>  <td>New</td> 
    <td>Sets transparent color for the lines selected in MXLS register.
      <BR>0 = Transparent<BR>1 = Black<BR>2 = <BR>3 = <BR>4 = Dark Grey <BR>5 = <BR>6 = 
      <BR>7 = Med Grey <BR>8 = <BR>9 = <BR>10 = Lite Grey <BR>11 = <BR>12-16 = White <br></td></tr>
  <tr><td>3-0</td>  <td>0000</td>  <td>New</td> 
    <td>Sets color #2 (med) for the lines selected in MXLS register.
      <BR>0 = Transparent<BR>1 = Black<BR>2 = <BR>3 = <BR>4 = Dark Grey <BR>5 = <BR>6 = 
      <BR>7 = Med Grey <BR>8 = <BR>9 = <BR>10 = Lite Grey <BR>11 = <BR>12-16 = White <br></td></tr>
</table>
<!-- ---------------------------------------------------------- -->
<BR><a name="MXM"></a><a href=#TOP>index</a><BR> 
<table style="width:100%">  <th style="width:15%"><b>MXM</b></th> <th style="width:10%"><b>0x37</b></th> <th><b>Mixer Mix Mode</b></th> </table>
<table style="width:100%">
  <tr>
    <th style="width:7%">BIT</th>
    <th style="width:8%">Default</th>   
    <th style="width:10%">Compat</th>
    <th>Function</th>
  </tr>
  <tr><td>7-2</td>  <td>0</td>  <td></td>  <td>Don't Care<br></td></tr>
  <tr><td>0-1</td>  <td>0x00</td>  <td>New</td>
    <td>Sets the way Layer0 and Layer1 interact when pixels overlap for the lines selected in MXLS register. 
    <BR>  0 = Layer 0 (text) will always display on top of layer1 (gfx)
    <BR>  1 = Layer 1 (gfx) will always display on top of layer0 (text)
    <BR>  2 = Will average the layers values. eg white+black=midgrey
    <BR>  3 = Layer 0 on top, Layer 1 adds 0,1,2,or 3 to the value of Layer 0. Used for greyscale mode.<br></td></tr>
</table>
<!-- ---------------------------------------------------------- -->
<!-- ---------------------------------------------------------- -->
<!-- ---------------------------------------------------------- -->
<BR><a name="SOS"></a><a href=#TOP>index</a><BR> 
<table style="width:100%">  <th style="width:15%"><b>SOS</b></th> <th style="width:10%"><b>0x38</b></th> <th><b>Servo Select</b></th> </table>
<table style="width:100%">
  <tr>
    <th style="width:7%">BIT</th>
    <th style="width:8%">Default</th>   
    <th style="width:10%">Compat</th>
    <th>Function</th>
  </tr>
  <tr><td>7-3</td>  <td>0</td>  <td></td>  <td>Don't Care<br></td></tr>
  <tr><td>2</td>  <td>0</td>  <td>New</td> <td>Selects Servo #3 for update.<br></td></tr>
  <tr><td>1</td>  <td>0</td>  <td>New</td> <td>Selects Servo #2 for update.<br></td></tr>
  <tr><td>0</td>  <td>0</td>  <td>New</td> <td>Selects Servo #1 for update.<br></td></tr>
</table>
<!-- ---------------------------------------------------------- -->
<BR><a name="SOP"></a><a href=#TOP>index</a><BR> 
<table style="width:100%">  <th style="width:15%"><b>SOP</b></th> <th style="width:10%"><b>0x39</b></th> <th><b>Servo Position</b></th> </table>
<table style="width:100%">
  <tr>
    <th style="width:7%">BIT</th>
    <th style="width:8%">Default</th>   
    <th style="width:10%">Compat</th>
    <th>Function</th>
  </tr>
  <tr><td>7-0</td>  <td>128</td>  <td>New</td>  <td>Sets Servo position.<br></td></tr>
</table>
<!-- ---------------------------------------------------------- -->
<BR><a name="SOW"></a><a href=#TOP>index</a><BR> 
<table style="width:100%">  <th style="width:15%"><b>SOW</b></th> <th style="width:10%"><b>0x3A</b></th> <th><b>Servo Width</b></th> </table>
<table style="width:100%">
  <tr>
    <th style="width:7%">BIT</th>
    <th style="width:8%">Default</th>   
    <th style="width:10%">Compat</th>
    <th>Function</th>
  </tr>
  <tr><td>7-0</td>  <td>200</td>  <td>New</td>  <td>Sets Servo travel width.<br></td></tr>
</table>
<!-- ---------------------------------------------------------- -->
<BR><a name="SOT"></a><a href=#TOP>index</a><BR> 
<table style="width:100%">  <th style="width:15%"><b>SOT</b></th> <th style="width:10%"><b>0x3B</b></th> <th><b>Servo Trim</b></th> </table>
<table style="width:100%">
  <tr>
    <th style="width:7%">BIT</th>
    <th style="width:8%">Default</th>   
    <th style="width:10%">Compat</th>
    <th>Function</th>
  </tr>
  <tr><td>7-0</td>  <td>128</td>  <td>New</td>  <td>Sets Servo trim.<br></td></tr>
</table>
<!-- ---------------------------------------------------------- -->
<BR><a name="DBUG"></a><a href=#TOP>index</a><BR> 
<table style="width:100%">  <th style="width:15%"><b>DBUG</b></th> <th style="width:10%"><b>0x3E</b></th> <th><b>Debug Register</b></th> </table>
<table style="width:100%">
  <tr>
    <th style="width:7%">BIT</th>
    <th style="width:8%">Default</th>   
    <th style="width:10%">Compat</th>
    <th>Function</th>
  </tr>
  <tr><td>7</td>  <td>0</td>  <td>New</td>  <td>Display Stack.<br></td></tr>
  <tr><td>6-2</td>  <td>0</td>  <td></td>  <td>TBD<br></td></tr>
  <tr><td>1</td>  <td>0</td>  <td>New</td>  <td>Display FPS Statistics.<br></td></tr>
  <tr><td>0</td>  <td>0</td>  <td>New</td>  <td>Display Irq Statistics.<br></td></tr>
</table>
<!-- ---------------------------------------------------------- -->
<BR><a name="EXE"></a><a href=#TOP>index</a><BR> 
<table style="width:100%">  <th style="width:15%"><b>EXE</b></th> <th style="width:10%"><b>0x3F</b></th> <th><b>Execute Buffer Register</b></th> </table>
<table style="width:100%">
  <tr>
    <th style="width:7%">BIT</th>
    <th style="width:8%">Default</th>   
    <th style="width:10%">Compat</th>
    <th>Function</th>
  </tr>
  <tr><td>7</td>  <td>0</td>  <td>New</td>  <td>Interpret <a href=#BUFF>BUFF</a> as a general command.<br></td></tr>
  <tr><td>6-5</td>  <td>0</td>  <td></td>  <td>Don't Care<br></td></tr>
  <tr><td>4</td>  <td>0</td>  <td>New</td>  <td>Interpret <a href=#BUFF>BUFF</a> as GOB #4 commands.<br></td></tr>
  <tr><td>3</td>  <td>0</td>  <td>New</td>  <td>Interpret <a href=#BUFF>BUFF</a> as GOB #3 commands.<br></td></tr>
  <tr><td>2</td>  <td>0</td>  <td>New</td>  <td>Interpret <a href=#BUFF>BUFF</a> as GOB #2 commands.<br></td></tr>
  <tr><td>1</td>  <td>0</td>  <td>New</td>  <td>Interpret <a href=#BUFF>BUFF</a> as GOB #1 commands.<br></td></tr>
  <tr><td>0</td>  <td>0</td>  <td>New</td>  <td>[*]Interpret <a href=#BUFF>BUFF</a> as a font character.<br></td></tr>
</table>
* not yet implemented.<BR>
<!-- ---------------------------------------------------------- -->
<BR><a name="BUFF"></a><a href=#TOP>index</a><BR> 
<table style="width:100%">  <th style="width:15%"><b>BUFF</b></th> <th style="width:10%"><b>0x40<BR>0x7F</b></th> <th><b>Data Buffer Registers</b></th> </table>
<table style="width:100%"><td>0x40<BR>0x7F</td> <td>BUFF</td> <td>Data Buffer Registers<BR><a href=#GFXCMD>Graphics Commands</a><BR><a href=#GENCMD>General Commands</a><BR></td></table>
<!-- ---------------------------------------------------------- -->
<BR><a name="GFXCMD"></a><a href=#TOP>index</a><BR> 
<b>Graphics Commands</b><br>
After writting up to 16 commands to <a href=#BUFF>BUFF</a>, you need to run the commands by setting a bit(s) in the <a href=#EXE>EXE</a> register to select which graphic object to modify.
All graphics are double buffered.  You can send multiple data packets without altering the display.  Changes are only displayed when a GFX_CMD_UPDATE command is encountered.
If you need to send less than 16 commands, terminate the command with GFX_CMD_END. 
<BR><BR>
<b>Format</b><br>

<table style="width:50%">

  <tr><th style="width:12%">CMD</th> <th style="width:7%">C2</th> <th style="width:7%">C1</th> <th style="width:37%">Y</th> <th style="width:37%">X</th></tr>
  <tr><td>4 bits</td> <td>2 bits</td> <td>2 bits</td> <td>12 bits</td><td>12 bits</td></tr>
</table>

<BR><BR><BR>
#define GFX_CMD_MOVE_TO  (1)<BR>
#define GFX_CMD_LINE_TO  (2)<BR>
#define GFX_CMD_BOX_TO   (3)<BR>
#define GFX_CMD_FRAME_TO (4)<BR>
#define GFX_CMD_PIXEL    (5)<BR>
#define GFX_CMD_TEXT     (8)<BR>
#define GFX_CMD_CLR      (13)<BR>
#define GFX_CMD_UPDATE   (14)<BR>
#define GFX_CMD_END      (15)<BR>

<BR>
#define GFX_CMD2(cmd,x,y)       (x|(y<<12)|(cmd<<28)) <BR>
#define GFX_CMD3(cmd,x,y,z)     (x|(y<<12)|(cmd<<28)|(z<<24))<BR>
#define GFX_CMD4(cmd,x,y,c1,c2) (x|(y<<12)|(cmd<<28)|(c1<<24)|(c2<<26))<BR>

 <BR><BR>
<!-- ---------------------------------------------------------- -->
<BR><a name="GENCMD"></a><a href=#TOP>index</a><BR> 
<b>General Commands</b><br>
<BR>
Write "BOOTLOADER" into <a href=#BUFF>BUFF</a> then set bit 7 in <a href=#EXE>EXE</a> : Enters DFU bootloader<BR>
<!-- ---------------------------------------------------------- -->
 <BR><BR> <BR><BR> <BR><BR> <BR><BR>
<!-- ---------------------------------------------------------- -->
</body>
</html>
