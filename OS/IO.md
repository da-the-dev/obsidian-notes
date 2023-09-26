![[Pasted image 20230912222419.png]]
# Interrupt
The driver starts the device and asks it to give an [[Interrupt|interrupt]] when it is finished. The operating system then blocks the caller if need be and looks for other work to do.

When the controller detects the end of the transfer, it generates an interrupt to signal completion. The device number may be used as an index into part of memory to find the address of the interrupt handler for this device. This part of memory is called the *interrupt vector*. 
