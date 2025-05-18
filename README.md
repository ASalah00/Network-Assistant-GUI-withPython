# Network-Assistant-GUI-withPython
This Python script, network_inventory_gui.py, is a PyQt6-based graphical application designed to help network administrators with two primary tasks: creating a network inventory and tracking devices by their MAC address.
Here's a breakdown of its capabilities and the information required to use it:
##Overall Purpose:
The application provides a user-friendly interface to interact with Cisco network devices using the Netmiko library. It automates the process of discovering network topology and locating specific devices.
Key Features:
##Network Documenter:
Task: Discovers Cisco switches connected in a network, starting from a specified distribution switch. It gathers information about each switch, including hostname, IP address, uplink connection, model number, serial number, and lists other detected neighbors.
###Capabilities:
Recursively traverses the network via CDP neighbors.
Handles multiple buildings/distribution switches in a single run.
Displays results in separate tabs for each building.
Exports the collected inventory data to an Excel spreadsheet (.xlsx).
Includes a "Remember Me" option to save the username.
Information Needed:
Username: The username required to log in to the network devices.
Password: The password required to log in to the network devices.
Building Name(s): A descriptive name for each network segment or building you want to document.
Distribution Switch IP(s): The IP address of the primary distribution switch for each building/segment where the discovery should start.
##MAC Tracker:
Task: Locates the network switch and specific interface to which a device with a given MAC address suffix is connected. It searches through the network by following trunk links based on MAC address table entries.
###Capabilities:
Traces a MAC address through multiple network hops.
Provides detailed logs of the tracking process.
Displays the final location (switch name, IP, and interface) of the device.
Includes an option to show more detailed technical logs for troubleshooting.
Includes a "Remember Me" option to save the username.
Information Needed:
Username: The username required to log in to the network devices.
Password: The password required to log in to the network devices.
Distribution Switch IP: The IP address of a switch (ideally a distribution switch near the potential location of the device) to start the search from.
Last 4 Digits of MAC Address: The last four hexadecimal characters of the MAC address of the device you are looking for (e.g., "BEEF").
