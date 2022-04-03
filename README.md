# Cryptocurrency
```
Part 2: Decentralize Blockchain to create a Cryptocurrency. 
```

## What is Cryptocurrency?
Cryptocurrency such as Bitcoin, Ethereum, Ripple, etc..., are Protocol that facilitates Blockchain technology and move it practice so that a network of people can transact with eachother. 

<img width="846" alt="Screen Shot 2022-04-02 at 7 47 01 PM" src="https://user-images.githubusercontent.com/25771787/161408998-a1ada7f4-5624-47df-bc66-4f53eb399c78.png">

## How to run the program
1. Either fork or download the code (each .py file represent a user/node)
2. Install all package: 
   - install [Flask](https://flask.palletsprojects.com/en/2.0.x/#)
     - Flask is a web framework used to build web application
   - install `requests 22.18.4` by typing `pip install requests==2.18.4` in terminal
   - download [Postman](https://www.postman.com)
      - Postman is an HTTP cline which provide a user freindly interface for making request
3. Open and run the applications (three python file) in any python IDE. `In other words, create three console in your IDE`

## How to interact with the apps using Postman
1. While the apps is running in your IDE. 
2. Open Postman and perform one of the following actions
    - create three tabs by `press the + icon in the builder or use the CMD/CTRL + T shortcut`
    - In each tab make a request to get the chain by `selecting GET enter the URL http://127.0.0.1:5002/get_chain click Send`
      - The address `127.0.0.1:5002` will change in `tab 2` to `127.0.0.1:5003` and `tab 3` to `127.0.0.1:5004` <img width="984" alt="Screen Shot 2022-04-02 at 9 45 10 PM" src="https://user-images.githubusercontent.com/25771787/161411930-5e1de830-a585-480e-ad0e-952deddbafb9.png">
    - Connect all user by `selecting POST. enter the URL http://127.0.0.1:5002/get_chain`
      - press the body, press raw, select JSON in the builder
    - enter the follow json codes in the body of each tabs than click **Send**:
      -  tab 1 enter `{"nodes": ["http://127.0.0.1:5003", "http://127.0.0.1:5004"}`
      -  tab 2 enter `{"nodes": ["http://127.0.0.1:5002", "http://127.0.0.1:5004"}`
      -  tab 3 enter `{"nodes": ["http://127.0.0.1:5003", "http://127.0.0.1:5001"}` <img width="941" alt="Screen Shot 2022-04-02 at 10 07 48 PM" src="https://user-images.githubusercontent.com/25771787/161412519-ad4dda64-70ea-4837-ba19-c4e10acffccb.png">




## Inportant concepts to understand
- Protocol is a set of rules that guide how participants of the network communicate with eachother.

- Participants used the Protocol (Bitcoin, Ethereum, Waves, etc...) to tranact with each other through mining and/or send/receiving tranaction. 
  - Some Protocol allow code (smart contracts) on the block. 

### Mining and Tranactions
1. [How Mining Work](https://www.investopedia.com/tech/how-does-bitcoin-mining-work/)
  - Mining is the process by which new bitcoins are entered into the circulation, it is also the way the network confirms new tranactions 
  - Miner are guessing difference **nonce** values until their value match a hash within the target set by the HASH Algorithm. 
<img width="840" alt="Screen Shot 2022-04-02 at 8 01 06 PM" src="https://user-images.githubusercontent.com/25771787/161409397-e036a886-6721-47d9-b422-950cf5c757f9.png">

2. [How Transactions work](https://bitcoin.org/bitcoin.pdf)
- Within the Protocol each owner transfers the **coin** to the next by digitally signing a hash of the previous transaction and the public key of the next owner and adding these to the end of the coin. A payee can verify the signatures to verify the chain of ownership.
<img width="859" alt="Screen Shot 2022-04-02 at 8 23 02 PM" src="https://user-images.githubusercontent.com/25771787/161409914-6f94d19a-c004-49de-b00d-1c2c2846ae8f.png">
- Each participants tranaction live on their **MEMPOOL** until its selected by a Miner
<img width="826" alt="Screen Shot 2022-04-02 at 8 28 15 PM" src="https://user-images.githubusercontent.com/25771787/161410034-90cba0a6-a299-4268-b73f-23866c731bda.png">

<img width="842" alt="Screen Shot 2022-04-02 at 8 27 23 PM" src="https://user-images.githubusercontent.com/25771787/161410013-16c75add-10ef-42d1-bcbb-d8316f99f027.png">
