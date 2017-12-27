# NextGen Government Election Platform  

> Based on Blockchain Technology

## Table of Contents

<!-- toc -->

- [Problem](#user-content-problem)
- [Solution](#user-content-solution)
- [Technology](#user-content-technology)
- [System Architecture](#user-content-system-architecture)
- [Contributing](#contributing)
- [Mobile App](#user-content-mobile-app)
- [Author](#author)

<!-- tocstop -->

## Problem

 Today’s election process requires heavy security, lacks transparency, polls are not updated in real-time, they are definitely not tamper proof and in some extreme cases, EVM machines are often accused of being hacked, in addition to all this, it is an extremely time consuming process where citizens are required to stand in long lines in the heat, cold, sun and rain in order to be able to cast their vote.

## Solution
Using blockchain technology we have solved this problem to ensure that the citizen voting process is :

- Secure - Using End to End Encryption and Tracking and Biometrics.
- Future Proof - Will be the foundation of all future voting processes. 
- Tamper Proof/Hack Proof - Using the Blockchain enabled ledger  
- Mobile - Can be ported to all types of hardware devices.
- Transparent - Using the Distributed Ledger Technology
- Quick - Fraction of the time required to cast a vote
- Empower the citizens to a seamless voting experience from "Booth to Result" in realtime.
- Flexible - Can be quickly customized to Suit all different requirements, from State elections to internal assembly elections to even on a national level.


## Technology

 So our E-voting  app is devided into five major component. 

 1. Ethereum running on AWS EC2 instance as pvt block.
 2. Nodejs Admin app Deployed over Heroku
 3. Vuejs Based Mobile app which can be installed as Android build
 4. A mongo as a service for database
 5. Adhaar Checksum for Adhaar validation (future use India-Stack)

 When an Admin registers we do following things 


  1. Create an Account on Ethereum server 
  2. When the response has come from geth we input the user in our Mongo Data base
     parameters : {"acountAddr","userAdhaar","Username","passKey"}
  3. Now when Admin has to login he has to enter Adhaar and passkey
  4. When he is logged in he is taken to a pannel where he can create Ballots
  5. The Ballot creation need three parameter in the constructor 
     {"Ballot Name","Start Time","Nominee List"} 
  6. After creating the ballot you can select the ballot and upload the Voter List which is string of Adhaar Id
  
  When user opens the mobile app

   1. He selects the Polls he want to vote for and enters his Adhaar Id
   2. We Check in the Contract if his Adhaar Id exist or not on Ethereum 
   2. if it exist he is taken to the ballot where here does the voting 
 

## System Architecture

![alt text](https://image.prntscr.com/image/wXd085nYTOqQAhsESZdM4w.png "System Architecture")


## Future Architecture Implementation . (Could be more scalable and basic security out of the box from aws) 

![alt text](https://image.prntscr.com/image/qqqB-2yWTzimjR3PVoc8NQ.png "Future Architecture")


## API
 ```
/**
 *  ------------Sample APIS-------------------
 * http://localhost:3000/api/create-ballot
 * http://localhost:3000/api/addparty
 * http://localhost:3000/api/parties-list
 * http://localhost:3000/api/add-voter
 * http://localhost:3000/api/validate-voter
 * http://localhost:3000/api/vote
 * http://localhost:3000/api/vote-count
 * http://localhost:3000/api/validate-adhar
 * http://localhost:3000/api/ballot-list
 * http://localhost:3000/api/admin-create
 * http://localhost:3000/api/admin-login
 * 
 */
```

![alt text](https://image.prntscr.com/image/22vMOGinRs_9i3QuQmRHKg.png "Register A Govt entity for polling")


They get an account and they can create Ballots .

![alt text](https://image.prntscr.com/image/Ss2fNcmjQUGmeBrBfSUt5g.png "Create Ballots")


They can upload Voter List for the ballot.

![alt text](https://image.prntscr.com/image/c2HDAaixTIGbBboWFqQwbA.png "Voter List")


User open's Installs mobile app and use his Adhaar Id for login .

![alt text](https://image.prntscr.com/image/U2ZWTdQKQnCOpNEc6LTUIQ.png "Voter Login Screen")
![alt text](https://image.ibb.co/n12bx6/Whats_App_Image_2017_12_26_at_1_58_03_PM.jpg "Voter Login Screen")

![alt text](https://image.prntscr.com/image/wHZZP5axRxmYvtFvyvmCoQ.png "Voter Ballot 1")
![alt text](https://image.prntscr.com/image/ivIP-ulvQp6038TrxJUg9w.png "Voter Ballot 2")
![alt text](https://image.prntscr.com/image/-BHGUiR_RqihwXFhZdolQw.png "Voter Ballot 3")



  ```


## Mobile App
 
 ```
  https://github.com/vikramIde/votingapp-mobile
  
  ```


## Author

**E-Voting** © [Vishwas1](https://github.com/Vishwas1), Released under the [MIT](./LICENSE) License.<br>
Authored and maintained by vikramIde with help from contributors ([list](Vishwas1/voting-daap-2017/graphs/contributors)).

The Team 

> [vick.Anand](https://facebook.com/vikramabhushan) · GitHub [@rapchik](https://github.com/vikramIde) · 

> [Vishwas.Anand](https://facebook.com/vikramabhushan) · GitHub [@Vishwas1](https://github.com/Vishwas1) · 

> [Harshitha.naidu](https://www.facebook.com/harshitha.naidu61) · GitHub [@harshitha](https://github.com/harshithanaiduk) · 
