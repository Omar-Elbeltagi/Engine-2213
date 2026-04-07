The circuit shown is a 4-bit multiplier:

The circuit is based on the concept of binary multiplication, where multiplication is performed by generating partial products and then adding them together. In binary, each bit of the multiplier is used to multiply the multiplicand, similar to decimal multiplication but using only 0s and 1s.

The operation in this stage is performed by the AND gates. Each AND gate takes one bit from the multiplicand (A4–A1) and multiplies it with the least significant bit of the multiplier (B1). In binary multiplication, this corresponds to multiplying the entire number A by a single bit B1.

If B1 = 1, the AND gates pass the values of A1–A4 directly to the output, forming the first partial product. If B1 = 0, all outputs become 0, effectively producing no contribution to the final result, the outputs of these AND gates represent: (AxB1) 
One of the outputs (S1) is connected to an LED through a resistor, providing a visual indication of the result of the least significant bit of this partial product.

