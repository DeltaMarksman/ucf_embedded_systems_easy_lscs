# ucf_embedded_systems_easy_lscs
Everything needed concerning leds, switches, and timer A module can now be done with the following functions:


// Config ACLK
config_ACLK_to_32KHz_crystal();

// CTRL Register setup
init_switches();                    // Init switches with resistors
init_leds();                        // Init registers for LEDs

// LED Manipulation
red_on();                           // turns on red led
red_off();                          // turns off red led
red_toggle();                       // toggles red led
green_on();                         // you get the idea
green_off();
green_toggle();

// Timer configuration
config_upmode(500);                 // Configure timer A to upmode going to x milliseconds, in this case 500
timer_callback([YOUR FUNCTION]);    // Which function to call every timer period. PASS IN THE FUNCTION ITSELF, DO NOT CALL IT

// Switch configuration
s1_callback([YOUR FUNCTION]);       // Which function to call when s1 is pressed. PASS IN THE FUNCTION ITSELF, DO NOT CALL IT
s2_callback([YOUR FUNCTION]);       // Which function to call when s1 is pressed. PASS IN THE FUNCTION ITSELF, DO NOT CALL IT
s1_pressed();                       // Returns 1 of s1 is pressed
s2_pressed();                       // Returns 1 of s1 is pressed

// Enable interrupts DONT FORGET THIS!
_enable_interrupts();
