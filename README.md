# Precision Pointer
This repository holds all of the code and hardware files for building a Precision Pointer unit (PPU). This repository is not fully ready to be public, so you may encounter errors or gaps in documentation -- however all the code needed to run the system (other than dependencies) can be found here.

## Building a PPU
Here's the general steps to replicating the system.
1. Buy the materials in `/Hardware Documentation/Bill of materials.csv`
2. Wire and assemble PPU. You will need to create additional mounts for the linear actuator. Again, see the files in the Hardware Documentation folder. See `pointer_driver/pointer_driver.ino` for pin definitions.
3. Connect to ArbotiX in Arduino IDE and upload `pointer_driver.ino`
4. Use `pointer.py` as an API interface to the PPU. `pointer_client.py` is also provided to provide remote control of a PPU connected to a remote machine.

---

# TODO
1. Remove Klampt dependency -- specifically replace `vectorops` operations.
2. Replace servo linear actuator with a digital servo motor. Specifically, use another dynamixel motor and translate the rotational motion to linear motion. This will provide far better consistency and accuracy for linear motion.
