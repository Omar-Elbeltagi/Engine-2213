Binary multiplication is a process of addition and shifting that mimics decimal long multiplication but uses only two digits, 0 and 1. The operation follows four simple rules: 0×0=0, 0×1=0, 1×0=0, and 1×1=1, meaning the product is 1 only when both inputs are 1<img width="387" height="382" alt="image" src="https://github.com/user-attachments/assets/e21a0e93-c074-471f-ac67-b9650db1b119" />

The circuit shown in the TinkerCad Picture is a 4-bit multiplier, designed based on this concept. Instead of directly multiplying numbers, the circuit generates partial products and then adds them together to produce the final result.
<img width="967" height="812" alt="4-bits Multipler- TinkerCad" src="https://github.com/user-attachments/assets/9a3677a6-7a6c-4565-ab92-2e4c182e23f8" />

The process begins with the least significant bit (LSB) of the multiplier (B1). This bit is combined with each bit of the multiplicand (A4–A1) using AND gates that follow the basic multiplication rules, producing the first partial product. If B1= 1, the multiplicand passes through; if B1 = 0, the result is all zeros.
<img width="630" height="1155" alt="Multiplication truth table" src="https://github.com/user-attachments/assets/fa43689d-502d-4016-918b-6b5d85e6b668" />

For the least significant bit "LSB" S1, the LED is connected to A1 B1, because there are no previous bits to add in that column, Any lower terms are effectively zero, so the result of that column is simply A1 B1.
<img width="590" height="377" alt="S1 LSB (A1 B1)" src="https://github.com/user-attachments/assets/eb0a4388-2da6-43ec-91d6-bd804e92496b" />

The same process is repeated for the remaining bits of the multiplier (B2, B3, B4). Each resulting partial product is then shifted to the left according to its bit position, just like in binary multiplication where each shift represents multiplication by a power of 2.
<img width="387" height="382" alt="Example of Binary multiplication process" src="https://github.com/user-attachments/assets/b0e8ccb0-00f7-4b35-85a5-b05e8d33236d" />

These shifted partial products are then added together using full adders, which combine the values and propagate carries between bits. This step ensures that all partial results are properly summed to produce the final binary product.

The outputs (S1, S2, S3, S4, S5, S6, S7, S8) represent the bits of the final result. Since multiplying two 4-bit numbers can produce up to an 8-bit output.

The truth table illustrates how the outputs change for different input combinations of A and B, confirming that the circuit correctly implements binary multiplication.
