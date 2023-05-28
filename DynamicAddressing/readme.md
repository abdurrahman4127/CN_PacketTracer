# DHCP Configuration in Packet Tracer

## Network Topology
![NetworkTopology](snapshots/network_topology.png)

## Task
The task is to configure DHCP (Dynamic Host Configuration Protocol) for automatic IP address assignment to network devices in Packet Tracer.

**Requirements**:
- The DHCP server should provide IP addresses in the range of `192.168.1.100` to `192.168.1.200`.
- The subnet mask for the network is `255.255.255.0`.
- The default gateway should be `192.168.1.1`.
- DNS server addresses should be configured as `8.8.8.8` and `8.8.4.4`.

## Steps

1. Add and configure a DHCP server:
   - Add a DHCP server device to the network topology.
   - Double-click the DHCP server to configure it.
   - Enter global configuration mode:

     ```
     enable
     configure terminal
     ```

   - Configure the DHCP address pool with the specified IP address range, subnet mask, default gateway, and DNS server addresses:

     ```
     ip dhcp pool netname
     network 192.168.1.0 255.255.255.0
     default-router 192.168.1.1
     dns-server 8.8.8.8 8.8.4.4
     exit
     ```

   - Save the configuration:

     ```
     write memory
     ```

2. Configure DHCP clients:
   - For each client device, open the configuration settings.
   - Set the IP address configuration to "DHCP" or "Automatic".
   - Save the configuration.

3. Test the DHCP configuration:
   - Start the simulation or real-time mode in Packet Tracer.
   - Verify that the client devices have obtained IP addresses from the DHCP server.
   - Ping the default gateway from a client device to ensure connectivity.
   - Verify that DNS resolution is working by visiting a website from a client device.

**Note**: Make sure that all devices are properly connected, and the DHCP server and client devices are on the same network segment.

## Additional Configuration

- To reserve specific IP addresses for certain devices, you can configure DHCP reservations on the DHCP server.
- You can also configure additional DHCP options such as lease time, domain name, and other parameters based on your requirements.

