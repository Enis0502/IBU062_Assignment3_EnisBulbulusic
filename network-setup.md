The devices in mz configuration are:
1 Router (1941)
2 Switches (2960)

On the 1st Switch there are:
1 PCs (168.90.0.3)
2 SERVERS (168.90.0.4 and 168.90.0.2)

On the 2nd switch there are:
2 PCs (210.3.14.3 and 210.3.14.4)
1 Laptop (210.3.14.2)
1 Server (210.3.14.5)

Updated:
Added 1 PC to each Switch
(168.90.0.5 and 210.3.14.6)

ROUTER INTERFACE CONFIGURATION:

    enable - Enter the right mode on the router for configuration.
    configure terminal — Enters into the global configuration mode.
    interface GigabitEthernet0/0 - Configure the GigaBitEthernet0/0 interface
    IP address 168.90.0.1 255.255.255.0 - Assigns an IP address and subnet mask to the interface
    No shutdown  - Reactivates the interface.

Do the same process with the GigabitEthernet0/1 interface.

Enable DHCP for each network:

    ip dhcp pool NET1 - Create a DHCP pool named NET1.
    network 168.90.0.0 255.255.255.0 - Assign a specific IP Address range for the DHCP pool.
    default-router 168.90.0.1 - Sets the default gateway for each device.  

    ip dhcp pool NET2  - Create another DHCP pool named NET2.
    network 210.3.14.0 255.255.255.0 - Assign a specific IP Address range for the DHCP pool.
    default-router 210.3.14.1 -Sets the default gateway for each device.  

And then manually set each node to DHCP instead of static Gateway.