# Tool: netInfo (netInfo())

## Working of netInfo tool.
1. Read the property content from ifcfg.conf file based on the Operating System.
2. Splits and store the file content in config_dict dictionary.
3. Modify some paramenters in config_dict like `ONBOOT, BOOTPROTO, and DEFROUTE`.
4. Inditify the current IP-Address and Subnet Prefix of the device.
5. Add new entries of IP-ADDR and PREFIX into the config_dict.
6. Write update dictionary to new net_ifcfg.conf property file.
7. Same dictionary data is also stored in net_ifcfg.json file.
8. Test the working platform like windows or linux.
9. Based on the platform runs following commands. <br/>
   - Windows - `powershell Get-Netroute , powershell Get-NetIPAddress`.
   - Linux - `ifconfig, netstat -r, nmcli general`
10. Commands result based on os is appended on net_ifcfg.conf file.
   

## Steps to run application on windows

**Requirements** - Latest Python version. <br />
**NOTE** - Since ifcfg.conf file is not supported in windows therfore, similar is created for the project.

1. Clone this repository to your local machine.
   ```bash
   git clone [https://github.com/Hrx717/Tool-netInfo-netInfo.git](https://github.com/Hrx717/Tool-netInfo-netInfo.git)
   cd Tool-netInfo-netInfo
   ```
2. Make sure to save the file.
3. Open terminal and run `python main.py` command or use code runner of VS-Code.
   ```bash
   python main.py
   ```

## Sample ifcfg.conf file

   ```bash
   TYPE="Ethernet"
   DEVICE="ens3"
   ONBOOT="no"
   BOOTPROTO="dynamic"
   DEFROUTE="yes"
   IPADDR=12.34.56.78
   GATEWAY=12.34.56.1
   NETMASK=255.255.255.0
   DNS1=108.61.10.10
   IPV6INIT="yes"
   IPV6_AUTOCONF="yes"
   ```
