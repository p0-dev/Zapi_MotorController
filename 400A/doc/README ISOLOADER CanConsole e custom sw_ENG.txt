SPECIFICATIONS AND PROCEDURES CUSTOM SOFTWARE ISOLOADER-MI-JACK "a4m/s_afk_3_id001":

Created custom SW isoloader version "a4m/s_afk_3_id001" and custom Console installer "ISOLOADERCanConsole213_install".

The changes compared to the standard concerned the inclusion of a new polynomial for level 2 authentication.
To activate LVL2, the password is “IsoLoader!” (without" ").
At the same time, after such authentication it is possible to manually change the parameters related to the calibration of the PWM sensor.
To eliminate the Calibration not performed alarm, it is also necessary to manually modify the "SENSOR ACQ.DONE" parameter.

Step-by-step procedure for manually entering agle offset:
1.Connect with ISOLOADERCANCONSOLE.

2.Enter password=IsoLoader! to activate writing the angle offset into memory.

3.When switching on, if the acquisition has never been done, the "OFFSET SPD.SENS." alarm appears.
"SPD.SENSOR OFFSET." (MDI/LED code = 3)
Causes:
It is necessary to acquire the offset angle between the stator and the speed sensor, i.e. they mutual angular misalignment.
An automatic function is dedicated to this procedure.
Troubleshooting:
Perform the teaching procedure. See paragraph 7.2.1.
7.2.1 Acquisition of absolute position sensors
Absolute position sensors (sin/cos, 3-Hall, resolvers) are crucial in the control of synchronous motors.
Amplitude and offset of analog signals and the relative angular offset between the sensor orientation and the motor
case must be properly set before starting a synchronous motor for the first time.

If it is not possible to perform sensor acquisition, to remove the "SENSOR SPD. OFFSET" alarm. you need to go and set it
manually the "SENSOR ACQ.DONE=ON" parameter.

4.Now it is possible to manually change the "OFFSET ANGLE" parameter manually to the value provided by the manufacturer of the electric motor,
or from the parameters csv file on which a sensor acquisition with a specific procedure had previously been performed via
ZpCanConsole.

5.Perform a save by clicking on "STORE".

6.Turn the key off and on again, receive the parameters and check that the values entered manually are correct.

7.Try to control the electric motor, checking that it turns correctly.
​
