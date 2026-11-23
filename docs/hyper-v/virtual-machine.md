# Hyper-V Virtual Switch Configuration

## Objective

Establish an isolated virtual network for the enterprise infrastructure lab using Hyper-V Virtual Switch Manager.

## Virtual Switch Types

Hyper-V supports three types of virtual switches:

| Switch Type | VM-to-VM | VM-to-Host | External Network |
|---|---|---|---|
| External | Yes | Configurable | Yes |
| Internal | Yes | Yes | No, by default |
| Private | Yes | No | No |

## Network Design Decision

An internal virtual switch was selected to allow communication between virtual machines and the physical host without directly connecting the lab to the physical home network.

This provides a controlled environment for experimenting with Active Directory, DNS, DHCP, and other enterprise network services.

## Switch Configuration

| Setting | Value |
|---|---|
| Switch Name | Lab-Internal |
| Switch Type | Internal |
| Network | 192.168.50.0/24 |
| Subnet Mask | 255.255.255.0 |
| Internet Access | Not configured |
| Hypervisor | Microsoft Hyper-V |

## Implementation

1. Opened Hyper-V Manager.
2. Selected Virtual Switch Manager.
3. Selected Internal as the virtual switch type.
4. Created a new virtual switch.
5. Assigned the name `Lab-Internal`.
6. Applied and saved the configuration.
7. Connected the DC01 virtual machine to the newly created switch.

## Verification

- Confirmed that Lab-Internal appeared in Virtual Switch Manager.
- Confirmed that DC01 was connected to Lab-Internal.
- Successfully configured DC01 with a static IPv4 address.

Communication between separate virtual machines will be tested when additional systems are deployed.

## Security Considerations

- The lab is not directly bridged to the physical home network.
- Experimental network services are contained within the virtual network.
- Internet access requires additional routing or NAT configuration.
- The physical host can communicate with lab systems when its virtual network adapter is appropriately configured.

## Lessons Learned

- Virtual switches provide network connectivity between virtual machines.
- Different switch types provide different levels of network accessibility and isolation.
- Network segmentation helps separate infrastructure environments.
- Internal virtual switches are useful for controlled infrastructure testing.

## Result

Successfully established an internal virtual network to support the enterprise infrastructure lab.