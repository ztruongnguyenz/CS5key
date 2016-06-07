# Remove trial key CS5

1.) Navigate to C:\Program Files\Common Files\Adobe\Adobe PCD
restart adobe cs5 trial delete PCD file

Adobe Common Files PCD Location

2.) Delete the file named “pcd”

3.) Open the “cache” folder

4.) Delete the file named “cache”

5.) Edit your “Hosts” file to prevent your Adobe CS5 programs from communicating with Adobe.

Editing your hosts file is a relatively easy task (See image below). Navigate to Computer -> Local Disk (C:) -> Windows -> System32 -> Drivers -> etc -> hosts. Or you can simply type “hosts” into the search bar when you are inside the folder “System32?.

You will need to change the security of the hosts file in order to edit it. Right click it, select properties and then select the security tab. You will need to grant regular users “Full Control” in order to edit this file.

WARNING: You should remove these full control privileges from the regular users group after editing the file for system security purposes.

Add the following lines to the bottom of the file:

127.0.0.1 activate.adobe.com
127.0.0.1 practivate.adobe.com

This essentially tells your computer that when you attempt to navigate to either activate.adobe.com orpractivate.adobe.com, rather than being directed to those addresses, your computer will loop that navigation back to itself, and your Adobe programs will fail to reach the adobe activation destination. “127.0.0.1? is your computers own loopback IP address.
edit windows hosts file for adobe activation

Click for full size

I’m actually not sure if that whole hosts file editing part is absolutely necessary, but it doesn’t seem like it could hurt. I’m not sure if Adobe attempts to keep track of trial users on their end.

Now the next time you open an Adobe CS5 program, you will be prompted to accept the license agreement and start a new trial.
