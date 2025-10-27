# Static Routing

## Objective
To understand routing principles and learn how to manually configure, verify, and troubleshoot static routes in Cisco networks to ensure efficient and secure packet forwarding between networks.

### Skills Learned

- Understand the Concept of Static Routing.
- Configure and Apply Static Routing in Network Design or Diagram.
- Troubleshoot Static Route Configuration.

### Tools Used
- I use VMware Workstation to run EVE-NG as an emulator for constructing and testing a Cisco lab environment.
- Putty for SSH.

## Steps
Step 1
- Design the topology:
  
  As we can see, i take two different place 1. Mumbai HQ and 2. Delhi Branch and draw a simple topology with two endpoint, those are connected with a unmanaged Switch and the Switch is connected with a Router <img width="307" height="36" alt="image" src="https://github.com/user-attachments/assets/d0a00800-1ae5-4b83-acdf-00b309d36666" /> .
  
*Ref 1: Network Diagram*
![Routing](https://github.com/user-attachments/assets/1b149ab6-bb4a-4730-9813-1d4f1bae2087)

Step 2
- Assing IP Address:

  As per the rules

 - Rules of basic connectivity
1. Gateway address & LAN network should be in same network.
2. Router ports facing each other should be in same network.
3. Every interface of a router should be in different netwokr.
4. Routers knows only its directly connected networks.

   I assign IP according to the requirments
   
   *Ref 2.1: Mumbai HQ and Delhi Branch*
   
   <img width="276" height="465" alt="image" src="https://github.com/user-attachments/assets/8fbbe94b-e89c-4bef-804d-55620c63ce32" /> <img width="287" height="450" alt="image" src="https://github.com/user-attachments/assets/b6133947-a97e-4b1a-9e96-e52885a1d6ca" />

Commands:

*Ref 2.2: Mumbai HQ and Delhi Branch*

<img width="297" height="315" alt="image" src="https://github.com/user-attachments/assets/58165c62-e5d9-435c-a313-286574a22b44" /> <img width="279" height="303" alt="image" src="https://github.com/user-attachments/assets/34dcb546-34c3-4535-aabe-37df242cc97e" />

Step 3
- Verify ping to Gateway:
  
  For Mumbai HQ ping from VPC5 and VPC6 to Gateway or Interface fa0/1

*Ref 3.1: Mumbai HQ*

  <img width="765" height="453" alt="image" src="https://github.com/user-attachments/assets/09f63b1a-bf26-4807-aa24-08f721935419" />

  For Delhi Branch ping from VPC7 and VPC8 to Gateway or Interface fa0/1

*Ref 3.2: Delhi Branch*

  <img width="935" height="459" alt="image" src="https://github.com/user-attachments/assets/532a8106-c6e9-4ed7-b873-c07f1b371f9d" />

Step 4
- Routing:
  
  *Ref 4: Routing between Mumbai HQ and Delhi Branch.*

  <img width="578" height="120" alt="image" src="https://github.com/user-attachments/assets/ca5ed7a9-0c7e-4a35-b712-696329654b45" />

- Command:

For Mumbai HQ : 
ip route 192.168.1.0 255.255.255.0 192.168.3.1
<img width="298" height="41" alt="image" src="https://github.com/user-attachments/assets/02b58fa6-6bac-48df-8e3a-8b059bbc2766" />

For Delhi Branch :
ip route 192.168.2.0 255.255.255.0 192.168.3.2
<img width="298" height="41" alt="image" src="https://github.com/user-attachments/assets/7a1894de-4d89-421f-9176-4621fc7c7cb0" />
