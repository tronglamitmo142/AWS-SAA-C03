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
- Using hub to connect devices, anything receiver on any hub's port is transmited on every other port => If multiple devices transmit at one time => collision => need to layer 2 

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
- Using ARP protocol 


