# ZeroTier-windows-exit-node
Tutorial how to create ZeroTier VPN Exit Node on windows

1. Install ZeroTier
1. Connect to network (auth in web)
1. in registry edit HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services\Tcpip\Parameters\IPEnableRouter set it to 1
1. reset PC
1. Open `ncpa.cpl`
1. Right click to primary network connection (Ethernet)
1. Go to Properties -> Sharing Tab
1. Enable Allow other network users to connect through this computer's Internet connection, and choose the ZeroTier network interface.
1. Reset Zerotier network interface
2. fix ip address automaticly set to your local network
1. Log in to ZeroTier Central
1. Add Routes
1. Destination `0.0.0.0/0`
1. Via `ZeroTier_IP_of_Exit_Node_PC`
1. Submit
1. On client devices open zerotier app and enable `Allow Default Route`
1. test connection
