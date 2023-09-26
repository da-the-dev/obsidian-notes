An interrupt is a signal emitted by a device or software that requires immediate attention from the processor. 
Interrupts can be triggered by hardware or software events, and they temporarily stop or terminate a service or a current [[Process|process]]. 
# Example
Request to disk
![[Pasted image 20230912222419.png]]
1. [[CPU]] issues a request for DMA (Direct Memory Access) controller to get some data at some address
2. DMA request disk controller for a data transfer to main memory.
3. Disk controller talks to a disk via a driver to get data and buffers it.
4. Disk controller transfers buffer to main memory
5. Disk controller notifies DMA that the transfer is done
6. DMA controller tells CPU to stop the interrupt