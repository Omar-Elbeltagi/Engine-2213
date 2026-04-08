The circuit performs both addition and subtraction using a 4-bit adder and 2’s complement logic.

The mode switch determines the operation when the mode is 0, the circuit performs normal binary addition, and when the mode is 1, it performs subtraction by converting the B into its 2’s complement form by passing each B input through XOR gates controlled by the mode signal.When the mode is 0, the XOR gates pass B unchanged. 

When the mode is 1, the XOR gates invert B, producing B′, at the same time the mode signal is connected to the carry-in of the Full-Adder, adding the required +1 to complete the 2's complement subtraction.
 <img width="462" height="223" alt="2&#39;s complement subtraction" src="https://github.com/user-attachments/assets/0252515b-7428-4275-ba99-3367364c13ec" /> ( 2's complement subtraction )
 <img width="480" height="270" alt="XOR Truth Table" src="https://github.com/user-attachments/assets/800597e7-43c2-4027-a289-668a463b1386" /> ( XOR Truth Table )

The adder then computes A + B (for addition) or A + B′ + 1 which is equel to A - B (for subtraction). The result is displayed through LEDs, where the least significant bit corresponds to S1 on the right and the most significant bit corresponds to S4 on the left. 
<img width="484" height="281" alt="Screenshot 2026-04-08 083114" src="https://github.com/user-attachments/assets/54ee7c41-01f8-40b0-9644-ae082d7196d3" /> ( TinkerCAD S4-S1)

The overflow detection logic monitors the MSB of A, B (A4, B4) and the result (S4). Overflow occurs when adding two positive numbers produces a negative result or when adding two negative numbers produces a positive result. This is detected using NOT, AND, and OR gates using the expration ( OverFlow = A4' B4' S4 + A4 B4 S4' ), and the overflow condition is dedicated by LED on the top of the MSB LED (S4).
<img width="327" height="188" alt="Overflow Truth Table" src="https://github.com/user-attachments/assets/0300dcfb-4347-48fa-9096-32bb24e1d5db" /> ( Overflow Truth Table )

However, my physical circuit on the breadboard did not work as expected, even though i copyied to TinkerCad and it worked correctly. I belive This difference may be due to the breadboard.

KiCAD Schematic:
<img width="1167" height="803" alt="KiCAD 2s 4-Bit Adder-Subtractor" src="https://github.com/user-attachments/assets/8c83db04-42dc-4451-a0be-6b4080f42866" />

TinkerCAD Circuit:
<img width="852" height="839" alt="Screenshot 2026-04-08 084514" src="https://github.com/user-attachments/assets/b4b3607c-8f52-4535-b0ad-76a3efda06ce" />
Linke : https://www.tinkercad.com/things/8nUD6ukh2LM-circuit-1-2s-4-bit-adder-subtractor-and-adder/editel?returnTo=https%3A%2F%2Fwww.tinkercad.com%2Fdashboard%2Fdesigns%2Fall&sharecode=UuFLs0HG28i60pQOT54KxYuwMzqBeTAeZaXYxLYVVgU

Physical Circuit on the Breadboard:
<img width="1280" height="960" alt="image" src="https://github.com/user-attachments/assets/25abf38d-e786-438b-aab0-d8600084d139" />
<img width="1280" height="960" alt="image" src="https://github.com/user-attachments/assets/c43a4b2e-c3f3-4d97-96cc-4c172bab70f4" />
<img width="1280" height="960" alt="image" src="https://github.com/user-attachments/assets/f9d2aa4e-a44b-4949-a9b3-d0cfe5e30adf" />







