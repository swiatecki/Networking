# Fiber WAN on Meraki MX84 

**Challenge:** On the Meraki MX84, only the two copper ports "Internet 1" and "Internet 2" can be used as WAN ports. However, if you are provided a fiber handoff, you need an external media-converter i.e. more equipment that can fail.

**Solution: (Workaround)** Use a SFP module for optical to electrical conversion, then create a VLAN between SFP port and a copper port an the switch - i used ports 9 and 11. 

Then connect a ethernet cable between the copper port and the WAN port - I used "Internet 2", but "Internet 1 will work equally fine".

Alltough this workaround is not pretty, nor port-efficient, it works!

Comments? I'm @swiatecki

## Lab Setup 
To test this i used the following setup

- Meraki MX84 
- Meraki 1000Base SX Multi-Mode SFP
- Allied Telesis AT MC1004 Media converter

![Picture of setup](https://raw.githubusercontent.com/swiatecki/Networking/master/MX84Fiber/setup.JPG)