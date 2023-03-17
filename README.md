# ArduinoBenderPCB_REMIX
Remix of PCB for Arduino controlled Wire Bender - Eagle Files

# NB NB : The PDF diagram is Mirrored! If you want to use this to make the PCB using Toner Transfer, You will need to mirror the PDF before Printing. 

A friend of mine wanted to build the AWESOME arduino controlled Wire Bender project by **How To Mechatronics**

project URL : https://howtomechatronics.com/projects/arduino-3d-wire-bending-machine/

But the provided PCB is Dual-sided. 

the PCB here is a Single Sided Version with thick tracks to help with Toner Transfer etc.

Please Note that Pin Assigments are changed if you use this PCB you will have to modify the code provided by the original project.

**Notable Changes :**

1. 7805 regulator has been removed as the Arduino NANO can regulate 12V with the built in regulator.
1. spare Digital pins D8 -- D12 have pads for optional pull up Resistors.
1. All Analogue Pins are broken out.
1. Stepper Driver Resolution is set via solder jumpers on the Copper side of the board.

if you use this PCB, please note the following changes need to be made in the Definition part of the Arduino Code.

ORIGINAL CODE 
-----------------
    // Define the stepper motors and the pins the will use
    AccelStepper feederStepper(1, 5, 6); // (Type:driver, STEP, DIR)
    AccelStepper zAxisStepper(1, 7, 8);
    AccelStepper benderStepper(1, 9, 10);


CHANGE TO
---------

    // Define the stepper motors and the pins the will use
    AccelStepper feederStepper(1, 6, 7); // (Type:driver, STEP, DIR)
    AccelStepper zAxisStepper(1, 4, 5);
    AccelStepper benderStepper(1, 2, 3);


LIMITATION OF LIABILITY 
-----------------------

Short version: We will not be liable for damages or losses arising from your use or inability to use the service or otherwise arising under this agreement. Please read this section carefully; it limits our obligations to you.

You understand and agree that we will not be liable to you or any third party for any loss of profits, use, goodwill, or data, or for any incidental, indirect, special, consequential or exemplary damages, however arising, that result from

the use, disclosure, or display of your User-Generated Content;
your use or inability to use the Service;
any modification, price change, suspension or discontinuance of the Service;
the Service generally or the software or systems that make the Service available;
unauthorized access to or alterations of your transmissions or data;
statements or conduct of any third party on the Service;
any other user interactions that you input or receive through your use of the Service; or
any other matter relating to the Service.
Our liability is limited whether or not we have been informed of the possibility of such damages, and even if a remedy set forth in this Agreement is found to have failed of its essential purpose. We will have no liability for any failure or delay due to matters beyond our reasonable control.

