# VLAN | Trunk | Traditional Inter VLAN | NAT

## Objective

Networking lab project we see which is to design and prove out a segmented enterprise network. I do this by creating VLANs on switches, configuring trunk links between switches and router, enabling routing for inter-VLAN traffic, and testing connectivity across Departments such as Management, Sales, and Operations. Configure NAT for internet access through end point devices. 

### Skills Learned
From this networking lab project i develop practical skills in designing segmented enterprise networks using VLANs, trunks, inter-VLAN routing, and NAT.

### Configuration Skills

- Create and assign VLANs (e.g., VLAN 10 Sales, VLAN 20 Marketing) to access ports.

- Configure DOT1Q trunks with encapsulation.

- Configure traditional Inter VLAN.

- Implement NAT (inside/outside interfaces, access-lists, overload pools) for endpoint internet access.

### Verification Skills

- Use show vlan brief, show interfaces trunk, show ip route, show ip nat translations, show int status, show int trunk

- Perform inter-VLAN pings, traceroutes, and endpoint connectivity checks.

### Design and Security Skills

- Segment broadcasts, isolate departments for security.

### Tools Used

- VMware

- EVE-NG

## Steps

- Step 1 (Network Diagram)

I create a network diagram where i take 1 router, 2 L2 switch, 4 end point device, those are connected with two switchs. Let assume those two switchs are situated in two didderent room or floor, now we have two different department sales and marketing. So i will create VLAN 10 for sales and VLAN 20 for marketing.

*Ref 1: Network Diagram*

![Topology](https://github.com/user-attachments/assets/fa75ce21-2aa6-47f1-8b36-9f4cbbd8b9b5)

- Step 2 (VLAN and Trunk port)

I creat and assign VLAN 10, 20 (VLAN 10 as sales and VLAN 20 as marketing) and Trunk to switch interface.

 Configuration for Switch 1 :-

<img width="338" height="230" alt="image" src="https://github.com/user-attachments/assets/1b75bfb2-dedf-40e0-b66b-bb7e2d1e3228" /> <img width="296" height="346" alt="image" src="https://github.com/user-attachments/assets/9b0aa77e-cf79-4a11-9634-421bba804650" />

 Configuration for Switch 2 :-

<img width="341" height="208" alt="image" src="https://github.com/user-attachments/assets/d1eb01ee-b7dc-47f3-89c0-13bbcd59cadb" /> <img width="302" height="359" alt="image" src="https://github.com/user-attachments/assets/4d844870-a4ea-40ea-a100-fa29aaf74d65" />

- Step 3 (Traditional Inter-VLAN)

Configure traditional Inter-VLAN on switch 1

<img width="388" height="117" alt="image" src="https://github.com/user-attachments/assets/188fe936-b43b-499d-8522-5cdc4b0f19b7" /> <img width="216" height="138" alt="image" src="https://github.com/user-attachments/assets/e2b5ac69-1f38-4eb0-a6ab-1d54cbc60d24" />

- Step 4 (Verify VLAN and Trunk port)

<img width="238" height="77" alt="image" src="https://github.com/user-attachments/assets/eb980342-375d-487c-a777-6c1158b50f41" />

![switch 1](https://github.com/user-attachments/assets/172f6189-9318-4e83-bc5c-5846c096238b)

![switch 2](https://github.com/user-attachments/assets/1dfa72c9-3efc-41a3-b82d-2dbba318d702)

- Step 5 (Router configuration)

Assign IP for router interface.

<img width="380" height="146" alt="image" src="https://github.com/user-attachments/assets/0939b6bb-62a5-4310-8073-8bd4f65b28bd" /> <img width="244" height="204" alt="image" src="https://github.com/user-attachments/assets/6d6a7dc3-6c5b-41ac-bba0-c5f6b7e79763" />

- Step 6 (Internet connectivity or NAT)

Configure inside/outside interfaces, access-lists, overload pools

<img width="146" height="415" alt="image" src="https://github.com/user-attachments/assets/3cc0bf91-1f8c-4367-9b79-a9a5dc857b03" /> <img width="360" height="323" alt="image" src="https://github.com/user-attachments/assets/943c2d3b-6471-42ea-9e14-2ca8a8e7ba36" />

- Step 7 (Assign IP to end point devices.)

Vlan_10_pc_1 (192.168.10.3)

Vlan_10_pc_2 (192.168.10.2)

Vlan_20_pc_1 (192.168.20.3)

Vlan_20_pc_2 (192.168.20.2)

- Step 8 (Check connectivity between same VLAN, Different VLAN, Internet from end point devices.)

First I ping from Vlan 10 pc 2 to gateway 192.168.10.1

Second ping to other end point device in same VLAN

Third ping to another end point device which is in different VLAN (VLAN 20)

![ping](https://github.com/user-attachments/assets/89842fdc-9f36-43fb-a67a-815b21870da5)

Check internet connectivity from end point device.

![nat](https://github.com/user-attachments/assets/e657f9b1-30c4-4e86-b7af-ad93e6792d8b)

