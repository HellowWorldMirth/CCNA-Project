# Advance Static Routing

## Objective
1. Connect all branches.
2. All network will communicate with each other.

### Skills Learned

- Understand the Concept of Static Routing.
- Configure and Apply Static Routing in Network Design or Diagram.
- Troubleshoot Static Route Configuration.

### Tools Used
- I use VMware Workstation to run EVE-NG as an emulator for constructing and testing a Cisco lab environment.
- Putty for SSH.

## Steps
Step 1
- Design the topology

As we can see, we have 3 branches in different location 1. Delhi, 2. Mumbai and 3. Channi. I draw a simple topology with two endpoint, those are connected with a unmanaged Switch and the Switch is connected with a Router. <img width="1215" height="656" alt="topology static routing 3 router" src="https://github.com/user-attachments/assets/861a2840-19d8-4c89-826a-7ec0a497d258" />

Step 2
- Assing IP Address:

  I assign IP according to the requirments.

- Commends:
  
<img width="269" height="388" alt="image" src="https://github.com/user-attachments/assets/3dd5cf0d-0df7-4bce-8ad0-e5a3cc4b1ca2" />
<img width="554" height="231" alt="image" src="https://github.com/user-attachments/assets/9799ae03-d5e7-4c3f-84a2-a7c13cbe573e" /> 
<img width="269" height="391" alt="image" src="https://github.com/user-attachments/assets/f5ae0650-4ff7-462e-b8cc-0e9bc6fbbb5d" />
<img width="548" height="237" alt="image" src="https://github.com/user-attachments/assets/98aed43d-da0f-4831-9624-e59355366a38" /> 
<img width="275" height="379" alt="image" src="https://github.com/user-attachments/assets/c0c55c8d-e77d-424b-9b28-a58fcbe6b495" />
<img width="481" height="428" alt="image" src="https://github.com/user-attachments/assets/2510e689-e34d-4c10-b804-f9382e2a61d4" />

Step 3
- Verify ping to Gateway:
  
For Delhi ping from VPC7 and VPC8 to Gateway or Interface fa1/0
<img width="700" height="629" alt="image" src="https://github.com/user-attachments/assets/86db2647-1075-497e-bcef-e588a9c2f763" />

For Mumbai ping from VPC9 and VPC10 to Gateway or Interface fa1/0
<img width="553" height="644" alt="image" src="https://github.com/user-attachments/assets/0cbfc5bc-3a31-45f3-8e13-00c340d27ac0" />

For Chennai ping from VPC11 and VPC12 to Gateway or Interface fa1/0
<img width="942" height="423" alt="image" src="https://github.com/user-attachments/assets/984013f2-cfca-4161-a75c-8f28d2a33ccc" />

Step 4
- Routing:

  *Routing between Delhi, Mumbai and Chennai.*
<img width="497" height="243" alt="image" src="https://github.com/user-attachments/assets/387ad64d-9152-4bf6-95da-8e52a378139f" />

- Command:

for Delhi:
 
<img width="388" height="158" alt="image" src="https://github.com/user-attachments/assets/0b75b220-189c-4cf2-8828-32e2f5f7c118" />

*Show ip int br*

<img width="642" height="145" alt="image" src="https://github.com/user-attachments/assets/7f7f6e76-f2d6-400a-b037-2734f13ec88b" />

*Show ip route*

<img width="640" height="341" alt="image" src="https://github.com/user-attachments/assets/567ef08e-7b47-46ce-91f7-0f37489f01ab" />

for Mumbai:

<img width="381" height="149" alt="image" src="https://github.com/user-attachments/assets/15bbb810-50eb-422e-81ce-a976ae86cd27" />

*Show ip int br*

<img width="645" height="168" alt="image" src="https://github.com/user-attachments/assets/ccd8986b-7685-45ca-88c8-d1edf74d20c3" />

*Show ip route*

<img width="641" height="333" alt="image" src="https://github.com/user-attachments/assets/bbab13d4-45bf-4e6c-a72c-95cbaba7d7c3" />

for Chennai:

<img width="386" height="162" alt="image" src="https://github.com/user-attachments/assets/e704db2b-65e5-4795-b63f-3a05180f9324" />

 *Show ip int br*

 <img width="645" height="144" alt="image" src="https://github.com/user-attachments/assets/6743bb92-a45e-4ce0-8288-4d65c4cfd092" />

 *Show ip route*

<img width="643" height="337" alt="image" src="https://github.com/user-attachments/assets/58e782fe-79bf-49a2-ba7c-999edfefca79" />

Step 5
- Ping Host to destination :

From Delhi (VPC7 192.168.1.2) to Mumbai (VPC10 192.168.3.2) and Chennai (VPC 12 192.168.2.2)

<img width="659" height="419" alt="image" src="https://github.com/user-attachments/assets/51dec62a-0bdf-4e13-95d6-319a73df1c28" />

From Mumbai (VPC9 192.168.3.3) to Delhi (VPC8 192.168.1.3) and Chennai (VPC11 192.168.2.3)

<img width="659" height="416" alt="image" src="https://github.com/user-attachments/assets/19eb2c30-f006-4f74-8bc8-30a68f8f690c" />

From Chennai (VPC11 192.168.2.3) to Delhi (VPC8 192.168.1.3) and Mumbai (VPC10 192.168.3.2)

<img width="661" height="418" alt="image" src="https://github.com/user-attachments/assets/18500c08-505c-4f6e-ad53-a8f56aab5f24" />

