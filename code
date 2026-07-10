#include <MD_Parola.h>
#include <MD_MAX72xx.h>
#include <SPI.h>

// ===== Display Configuration =====
#define HARDWARE_TYPE MD_MAX72XX::FC16_HW
#define MAX_DEVICES 4

// ESP32 SPI Pins
#define DATA_PIN 23   // DIN
#define CLK_PIN  18   // CLK
#define CS_PIN   5    // CS

// Create display object
MD_Parola P = MD_Parola(HARDWARE_TYPE, CS_PIN, MAX_DEVICES);

void setup()
{
  P.begin();
  P.setIntensity(5);        // Brightness (0-15)
  P.displayClear();
}

void loop()
{
  if (P.displayAnimate())
  {
    P.displayText(
      "HELLO WORLD",
      PA_LEFT,
      50,          // Scroll speed
      1000,        // Pause time
      PA_SCROLL_LEFT,
      PA_SCROLL_LEFT
    );
  }
}
