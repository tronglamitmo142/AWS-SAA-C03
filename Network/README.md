## Encryption 
2 types of encryption:  
- Encryption at Rest: Encrypt in device, hardware, storage  
- Encryption at Transit: Protecting data when they transit over network   

### Symmetric Encryption  
- Encryption and Decryption using same key   
- Useful for **Encryption at Rest**   
- Not useful for **Encryption at Transit** (easy to retrive key through network)

### Asymmetric Encryption 

1. Client and server agree the same algorithm to use   
2. Create 2 key: public and private:     
   - Anyone has public key can create cyphertext  
   - Ciphertext only be decrypted by Private key      

3. Signing  
   - To prove the ciphertext is sent by right devices     
   - Sign by private key -> prove by public key     

## Networking       
### Layer 1     
- Physical medium can be cooper, fibre, wifi  
- Using hub to connect devices, anything receiver on any hub's port is   transmited on every other port => If multiple devices transmit at one time =>   collision => need to layer 2   

### Layer 2  
- Unit is Frame   
| Preamble (56 bits) | Destination MAC | Source MAC | ET 16 bits | PayLoad | FCS (Check  Sequence) |    
- Provide Control Access (Media access control)     
  - Create a frame with source-destination MAC Adrress    
  - Check Carrier (Carrier Detect):    
    - If no carrier -> send data     
    - if has -> waiting     
    => Prevent collison   
- Send data   
- Layer 2's network device: Switch with Mac Address Table  
  | MAC | PORT |   
- Using ARP protocol:  
  - Run between layer 2-3  

### Layer 3  
- Data Unit: Packet   
- IP Protocol   
- Some important field:  
  - TTL (Time to live)  
  - Protocol   
  - Source IP Address  
  - Destination IP Address   
- Subnet mask: Allow hosts to determinie if an IP address it need communicate   with local or remote => need to use default gateway or locally   
- Route table rule: The more specifixes are prefered (0 lowest, 32 highest).   
- Limitation of Layer 3:   
  - No method for channels of communication => Only 1 communication in one time => Only can connect 1:1 => not reliable   
  - Each packet is routed independently  
=> Need to layer 4 to resolve   

### Layer 4  
- TCP/IP: Using TCP above IP protocol  
- Some important fields:  
- Segment guaranties packet is transmited with right sequence   

### Network address Translation (NAT)  
- Only for IPv4  
- 3 types:  
  - Static NAT: 1 private -> 1 fixed public address   
  - Dynamic NAT: 1 private -> 1st public address   
  - Port Address Translation (PAT) -> many private -> 1 publicc (Using NAT Table)
    | Private IP | Private Port | Public IP | Public Port | 

### IP Addresing and IP Subneting 
- 0.0.0.0 -> 255.255.255.255 ~ 4,3 billion devices
- All public IPv4 need to be allocated manually 
- Class A: 0.0.0.0 -> 127.255.255.255 ~ 16,7 million network. Using for large bussiness, large organization 
- Class B: 128.0.0.0 -> 191.255.255.255 ~ 16,300 Network. For smaller bussiness than A 
- Class C: 192.0.0.0 -> 233.255.255.255   
- 3 private range often use:  
  - 10.0.0.0 - 10.255.255.255 (1 x class A)  
  - 172.16.0.0 - 172.32.255.255 (16 x class B)  
  - 192.168.0.0 - 192.168.255.255 (256 x class C)  
### Subneting  
- Breaking Network into smaller pieces: /16 -> 2 * /17  
- SLL & TLS:  
