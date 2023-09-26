1. **BIOS** (Basic Input Output System) is a program on the parent board that contains low-level I/O software
2. **POST** (Power-On Self-Test) is an integrity test that check the status of the system and reports errors. Run after BIOS.
3. POST first scans all [[Bus|busses]] to find devices and then selects a boot device for CMOS memory.
   CMOS is Complementary metal-oxide-semiconductor
4. The boot sector is read into the memory and executed. This sector contains a program that checks the last sector and examines the partition.
5. A **secondary boot loader** is read from that partition. It load the OS and start is. OS takes the driver configuration from BIOS. 
6. Once all device drivers are found by the OS, it loads them into the kernel. Autostart [[Process|processes]] are launched.