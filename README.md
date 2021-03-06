nano11Uxx (LPC11U3x + nRF BLE)
===============================

uCXpresso.BLE RTOS C/C++ Framework for Bluetooth Low Energy

v1.0.4 released 13th April 2014
--------------------------------
###Features:
	1. Update I2C driver and compatible with I2Cdevlib.
	2. Add a simple gabrage collector template class.
	3. Update the power-save scheme.

###Details:
	1. Add DCMotor class in "/extensions/lib/motor/h-bridge".
	2. Add ADXL345 and MPU-6050 I2C sensor devices in "/uCXpresso.BLE/extensions/lib/sensor".
	3. Move readwrite member from CI2CMaster to CI2C base class.
	4. Fixed I2C lock problem and shift left address bit for Arduino definition.
	5. Add more read and write member functions in CI2CMaster class.
	6. Add Garbage Collector Handle Template Class : gcHandleT<CType>
	7. Update Doxygen Documents.


v1.0.3 released 20th March 2014
--------------------------------	
###Features:
	1. Use interrupt to handle the BLE core, and puhs BLE in to BLOCK status when BLE is in idle mode.
	2. CSerial (UART) and usbCDC classes supports the semaphore to control the FIFO buffer.

###Details:
	1. Add more operators in CStream class.
	2. Add fifo semaphore control in CSerial and usbCDC classes.
	3. Increase more heap memory
	4. Change BLE polling to interrupt method to speed up the BLE core.
	5. BLE become to a Weakup Source for Power Save Features.


v1.0.2 released 13th March 2014
--------------------------------
###Features:
	1. When host APP crash or other, the BLE will lock in a invalid connection loop.
	   This version add a Watchdog feature on a BLE connection, 
	   the watchdog will force to disconnect a invalid connection.
	2. We provide a offline manual in the "doc" folder for reference.
	
###Details:
	1. Add "doc" folder in "/uCXpresso.BLE" framework.
	2. Add doxygen class manual and getting started document in "doc" folder.
    3. Add BLE ACI queue buffer (use CMailBox class)for BLE core transaction. (More Speed up & smooth)
    4. Add non static post() member function in CMailBox class.
    5. Add watchdog in BLE core, default watchdog timeout is 10 seconds.
    6. Add onWatchdog Event in bleSerial class, call back when App crash and BLE core WD timeout.
    7. Add onError Event in bleSerial class to indicate the BLE core error information.
    8. Move setTxPowerLevel service from bleSerail to bleProxmity class.
    9. Build by GCC 4.8.3 
	10. Update ble examples projects XML with LPCXpresso v7.0.0 
