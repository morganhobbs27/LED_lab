/* 
 * Project myProject
 * Author: Colby and Morgan
 * Date: 
 * For comprehensive documentation and examples, please visit:
 * https://docs.particle.io/firmware/best-practices/firmware-template/
 */

// Include Particle Device OS APIs
#include "Particle.h"

// We define MY_LED to be the LED that we want to blink.
//
// In this tutorial, we're using the blue D7 LED (next to D7 on the Photon
// and Electron, and next to the USB connector on the Argon and Boron).
const pin_t MY_LED = D7;

// The following line is optional, but recommended in most firmware. It
// allows your code to run before the cloud is connected. In this case,
// it will begin blinking almost immediately instead of waiting until
// breathing cyan,
SYSTEM_THREAD(ENABLED);
SYSTEM_MODE(SEMI_AUTOMATIC);

// Random note to show git tools

// The setup() method is called once when the device boots.
void setup()
{
  // Particle.disconnect();
  // WiFi.off();
	// In order to set a pin, you must tell Device OS that the pin is
	// an OUTPUT pin. This is often done from setup() since you only need
	// to do it once.
	pinMode(MY_LED, OUTPUT);
}

// Helper function to blink a dot (short)
void dot() {
	digitalWrite(MY_LED, HIGH);
	delay(200);  // Dot duration
	digitalWrite(MY_LED, LOW);
	delay(200);  // Gap between symbols
}

// Helper function to blink a dash (long)
void dash() {
	digitalWrite(MY_LED, HIGH);
	delay(600);  // Dash duration
	digitalWrite(MY_LED, LOW);
	delay(200);  // Gap between symbols
}

// Helper function to create gap between letters
void letterGap() {
	delay(400);  // Additional gap to total 600ms between letters
}

// The loop() method is called frequently.
void loop()
{
	// S: three dots
	dot();
	dot();
	dot();
	letterGap();

	// O: three dashes
	dash();
	dash();
	dash();
	letterGap();

	// S: three dots
	dot();
	dot();
	dot();
	letterGap();

	// Long pause before repeating
	delay(1s);
}
