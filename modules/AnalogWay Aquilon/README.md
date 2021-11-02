# AquilonAWJProtocol

### Version: 1.4.0

AquilonAWJProtocol module is a module for controlling AnalogWay LivePremier in combination with AquilonAWJProtocolHelper module.

## Installation

1. Import the module by pressing the plus down in the left corner of Pixera Control.
2. Drag it to the viewport of Control.

## Commands

- Take
- Control T-bar
- Recalling master preset memories
- Recalling screen preset memories
- Change layer source
- Change routing audio source
- System commands

## Usage

1. Set the IP in the propertie of the AquilonAWJProtocol module to the IP address of Aquilon.
2. Press "init()" and check that "IsConnected" is displayed as "true".  
If "IsConnected" does not display "true", press "uninit()" once and then press "init()" again.
3. Confirm that the screen enabled in Aquilon is displayed as "true" in the screen of the "GetScreenStatus" folder.  
If the enabled screen is displayed as "false", press "StartupGetActiveScreen ()" to update the screen status. 
4. The AquilonAWJProtocol module operates by monitoring the position of Aquilon's virtual T-bar, so after pressing TAKE to switch between PGM and PRW, set the time to check the position of the virtual T-bar to "TakeTime" in milliseconds.
5. Connect the AquilonAWJProtocol of the action that sends the command to Aquilon and the action of AquilonAWJProtocolHelper.  
When controlling the T-bar with the slider of Pixera's UI, set the slider value from 0 to 65535. In addition, it is necessary to connect the action of "T-bar Status" of AquilonAWJProtocol and AquilonAWJProtocolHelper.  
When use action of TAKE, there is no command to monitor the position of the virtual T-bar in the individual screen Take action of AquilonAWJProtocol module, so it is necessary to perform TAKE in combination with the action of AquilonAWJProtocolHelper module.

## AquilonAWJProtocolHelper

### Version: 1.4.0

AquilonAWJProtocolHelper is a support module for AquilonAWJProtocol.  
When changing the module name of AquilonAWJProtocol, it is necessary to change the code in "Trigger" of each screen of "toTAKE" and the code in TBAR of "toTBAR". 

## Usage

Connect to the action of AquilonAWJProtocol.  
Folders names starting with "to" are actions for connecting to the AquilonAWJProtocol module from action and sending integer or string value.  
Folders names starting with "from" are for connecting from the action of the AquilonAWJProtocol module and using UI buttons in custom CSS to change the display of the buttons.  

## Dependencies

The used Pixera version 1.8.RC7  
The used Aquilon version 2.2.79

## Test

The [LIVEPREMIER SIMULATOR](https://www.analogway.com/apac/training-support/telechargements/livepremier%E2%84%A2-simulator/id:401/) can be used to test.

## License

[MIT License](https://github.com/pixera-one/control-modules/blob/main/LICENSE)

This is a third-party community module, therefor AV Stumpfl and AnalogWay will not provide any direct support for this module.

## Author

[Yosuke Kikukawa](https://github.com/YosukeMW)