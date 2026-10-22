# Buddy Board

This simple add-on module allows the logical combination of 2 MakeACS card readers, to help with enforcing buddy policies or operator handovers. Operating modes include;
* AND: Both card readers need a valid user to unlock the deployment. Good for forcing 2 users to be present.
* OR: Either card reader can unlock the deployment. Good for letting users handoff wiithout interrupting the operation.
* AND-OR: Both card readers need a valid user to unlock the deployment, but then only one card reader is needed to keep it active. Good for complex equipment where you want sometime to look over the setup/startup, but then can leave one operator to take care of it.

The AND/OR/AND-OR operation only happens on the Access signal. All other bus signals are passed to the "Primary" card reader. The "Secondary" card reader is only used for its Access signal. Both devices have a OneWire unique ID on their OneWire bus to identify the Buddy Board, and both interrupt busses are tied together, so either Core can assert an interrupt or respond to an interrupt. 

The mode of operation is selected by jumpers on the board. 

## License
This project is licensed under the CERN-OHL-S 2.0 License. See LIECENSE.txt for more information.
