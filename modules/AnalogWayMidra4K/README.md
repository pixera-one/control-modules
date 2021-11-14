# Midra4KAWJProtocol

### Version: 1.2.1

Midra4KAWJProtocol module is a module for controlling AnalogWay Midra4K in combination with Midra4KAWJProtocolHelper module.

## Installation

1. Import the module by pressing the plus down in the left corner of Pixera Control.
2. Drag it to the viewport of Control.

## Commands

- Take
- Control T-bar
- Recalling master preset memories
- Recalling screen preset memories
- Change layer source
- Change image slot
- Change audio source
- System commands

## Usage

1. Set the IP in the propertie of the Midra4KAWJProtocol module to the IP address of Midra4K.
2. Press "init()" and check that "IsConnected" is displayed as "true".  
If "IsConnected" does not display "true", press "uninit()" once and then press "init()" again.
3. The Midra4KAWJProtocol module operates by monitoring the position of Midra4K's virtual T-bar, so after pressing TAKE to switch between PGM and PRW, set the time to check the position of the virtual T-bar to "TakeTime" in milliseconds.
4. Connect the Midra4KAWJProtocol of the action that sends the command to AquilonMidra4K and the action of Midra4KAWJProtocolHelper.  
When controlling the T-bar with the slider of Pixera's UI, set the slider value from 0 to 65535. In addition, it is necessary to connect the action of "T-bar Status" of Midra4KAWJProtocol and Midra4KAWJProtocolHelper. 

## Midra4KAWJProtocolHelper

### Version: 1.2.1

Midra4KAWJProtocolHelper is a support module for Midra4KAWJProtocol.  
When changing the module name of Midra4KAWJProtocol, it is necessary to change the code in TBAR of "toTBAR". 

## Usage

Connect to the action of Midra4KAWJProtocol.  
Folders names starting with "to" are actions for connecting to the Midra4KAWJProtocol module from action and sending integer or string value.  
Folders names starting with "from" are for connecting from the action of the Midra4KAWJProtocol module and using UI buttons in custom CSS to change the display of the buttons.  

## Dependencies

The used Pixera version 1.8.RC7  
The used Midra4K version 2.0.20

## Test

The [MIDRA4K SIMULATOR](https://www.analogway.com/apac/training-support/telechargements/midra%E2%84%A2-4k-simulator/id:433/) can be used to test.  
MIDRA4K SIMULATOR does not execute commands that control the T-bar. 

## License

[MIT License](https://github.com/pixera-one/control-modules/blob/main/LICENSE)

This is a third-party community module, therefor AV Stumpfl and AnalogWay will not provide any direct support for this module.

## Author

[Yosuke Kikukawa](https://github.com/YosukeMW)