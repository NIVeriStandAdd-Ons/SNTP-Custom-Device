## SNTP-Custom-Device ##

This is an example of how to adjust NI Target System-Time (running PharLap) using SNTP protocol.

With default settings, the RT-Driver makes a request to SNTP server every 40 seconds. Then it computes a correction to apply to local System-Time. This correction is applied every 10 seconds with a maximum Offset (cf. later).

NOTES:
- In order to use it, compile the Configuration and Engine part and instance the Custom Device in NI-VeriStand.
- IP Address of SNTP server is not exposed directly to user via User Interface, it's coded as a property in Initialization VI.
- In System Explorer, on Target page, option "Filter Watchdog Error" should be set to avoid -307732 error.
- In RT Driver VI, no correction is applied if Offset from Time Reference is in [-0.001; 0.001] second range.
- There is a property "Maximum Offset To Apply" initialized in Initialization VI that allows to put a maximum offset applied.

### LabVIEW Version ###

LabVIEW 2013
Code version 1.2.

### Built Availability ###

Users are allowed to build anything under Build Specifications in the source's LabVIEW project(s). There is no built version supplied.

### Quality, Limitations ###

IP has been tested by developer.

### Dependencies ###
This Custom-Device requires somes VIs from "Absolute Time" sub-palette in "Timed Structures" palette from "Structures" palette.
These VIs are part of an installer which can be found here:
https://decibel.ni.com/content/projects/ni-timesync-custom-time-reference
Please NOTE that a manual copy must be made to have the VIs for 2013 version. A post at the bottom of the page explains the process for 2012, apply it but for 2013.

### License ###

*This repository and any materials provided by NI therein are provided AS IS. NI DISCLAIMS ANY AND ALL LIABILITIES FOR AND MAKES NO WARRANTIES, EITHER EXPRESS OR IMPLIED, INCLUDING WITHOUT LIMITATION ANY WARRANTIES OF MERCHANTABILITY, FITNESS FOR  PARTICULAR PURPOSE, OR NON-INFRINGEMENT OF INTELLECTUAL PROPERTY. NI shall have no liability for any direct, indirect, incidental, punitive, special, or consequential damages for your use of the repository or any materials contained therein.*
