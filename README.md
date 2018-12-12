# nRF52_Simple_ACK_Demo
A simple sender and receiver demo using an ACK protocol to ensure that 
all payloads sent are received.

DESCRIPTION: this nRF52 Forth code demonstrates a simple transmitter 
node and a simple receiver node using an ACK protocol to ensure that
every transmitted payload is received.
  
The transmitter increments a counter and then transmits it.  If the
transmitter does not receive an ACK from the receiver within 250
microseconds, it repeats the process, but with the same counter.  If
the transmitter does receive an ACK within the expected timeframe,
it will increment the counter and repeat.

For its part, the receiver node will immediately ACK any packet
addressed to it and then print the counter that's in the payload.


DIRECTIONS: 
1. Load the current versions of the following files:
   i.   https://github.com/rabbithat/nRF52_delay_functions
   ii.  https://github.com/rabbithat/nRF52_essential_definitions
2. Only after loading the above files, load this file.
3. At the REPL prompt, type 'tx' to create a transmitting node, or 'rx' 
   to create a receiver node. For a proper demonstration, you will need 
   one node of each type.
