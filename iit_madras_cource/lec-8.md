## Bit manipulation
- CPU is designed to handle the data of size of word (8 bits, 16 or 32 bits), and not for a single bit.
- Set a bit: this means to set a certain bit in a word to **1**.
- Logic
```
1. Get the old value.
2. Set the desired bit to 1.
3. Store the new value back.

How to do it in c:
1. Create a bitmask. 1 << bit_position
2. data = data | (1 << 3). [Example code for setting 3rd bit]
```
- Clear a bit: set a bit to **0**
- Logic
```
1. Create a bitmask of ~(1 << bit_position)
2. Perform logical AND with the data
3. data = data & ~(1 << 4 ). [Example of setting 4th bit to 0]
```

- Toggle a bit: this changes the bit from 0 to 1 or 1 to 0.
- Logic:
```
1. Create a bitmask of (1 << bit_position)
2. Perform logical XOR operation with the data (XOR outputs 0 if both input are same, and 1 if both input are different)
3. data = data ^ (1 << 5). [Example of toggling the 5th bit]
```

- Check if a perticular bit is set or not
- Logic
```
1. Create a bitmask of (1 << bit_position)
2. Perform a logical AND operation with the data
3. Check if the result is zero or not. If it's 0 then bit is not set, else it is set
4. result = data | (1 << 6)
5. result != 0
```
