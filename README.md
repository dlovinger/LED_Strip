# LED_Strip

In line #420: NeoPatterns strip(120, 6, NEO_GRB + NEO_KHZ800, &StripComplete);
Redefine the number of pixles (120), the data pin on the microcontroller (6) and the type of LED strip you have (GRB, RGB, etc).
As well as the pin the button is connected to in line #431.

In line #457, strip.setBrightness(25); is a global brightness control (1-255). Keep it low to ensure you're not pulling too much current from the power source. Each pixel can pull up to 60mA at full white brightness (color (255,255,255)). Typical colors are ~40mA at full brightness. At a lower global brightness, you may be pulling ~3-5mA from each, which still adds up to a large curent draw. 
