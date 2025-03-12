- key is pressed from the keyboard equivalent ASCII character value will be decoded to special register called KBD_DATA. set flag KIN (Keyboard Input) to 1 indicating new data to be read.

- Processor runs a program constantly at the processor, checks KIN flag if KIN is 0, no new data, if KIN is set to 1, reads a character from KBD_DATA into register.

- After reading a character, keyboard hardware automatically resets KIN back to 0.

- The output process, DISP -> DOUT to 1. If the DOUT is set to 1 then it is ready to display a chearacter.

- processor checks DOUT flag. if DOUT is 0, it keeps waiting for the next input. If it is set to 1, processor takes the character from register and sends it to register display data.

- CLEAR command sets DOUT to 0