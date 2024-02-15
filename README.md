# Datalogger Code
 Example datalogger program for Campbell Scientific CR1000X

CR_Basic code is used to program the Campbell Scientific CR1000X datalogger.  The program can be edited in LoggerNet (a Campbell Scientific supplied editor).

Program "Lys_V1_2e_example" is currently used in field deployed lysimeters and is capable of measuring two lysimeters, each having the following sensors: one load cell, one type-T thermocouple, one fluid level transducer, one 12-VDC submersible pump and two soil sensors.
Revision notes are included at the top of the program, followed by a wiring diagram.  Various documentation notes are included within the code.
Current conditions are written to a text file on the CPU drive of the datalogger (CPU:Example_current.txt), where "Example" can be changed to reflect the site name, or experiment, or ...  If the text file cannot be found then hard coded initial conditions are assumed; these values in the code should be changed based on the lysimeter calibration multiplier, transducer calibration, lysimeter soil tank area, Tare weight, and stage datum.

Set the boolean "calib" = True during lysimeter calibration; this will record values avery 10-seconds during the active calibration of the lysimeter.  Otherwise leave the boolean variable = false to save memory on the datalogger.

