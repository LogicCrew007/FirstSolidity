//SPDX-License-Identifier:MIT
pragma solidity ^0.8.0;
import "erc201.sol";
contract Plane{
    MyToken PIAtoken;
     constructor(address _PIAtoken){
        PIAtoken=MyToken(_PIAtoken);
     }
    struct PlaneCompany{
        string CompanyName;
        string FlightNO;
    }
    PlaneCompany public Company;
    uint public Rate;

    function CompanyInfo(string memory _CompanyName,string memory _FlightNO)public{
       Company.CompanyName=_CompanyName;
       Company.FlightNO=_FlightNO;
       if (keccak256(abi.encodePacked(_CompanyName)) == keccak256(abi.encodePacked("city"))){
          
         if (keccak256(abi.encodePacked(_FlightNO)) == keccak256(abi.encodePacked("20"))){
             Rate=100000;

         PIAtoken.transfer(msg.sender,1000);
         }
   }
        else if (keccak256(abi.encodePacked(_CompanyName)) == keccak256(abi.encodePacked("cultus"))){
          
         if (keccak256(abi.encodePacked(_FlightNO)) == keccak256(abi.encodePacked("19"))){
           Rate=1000;
         PIAtoken.transfer(msg.sender,100);
    
        
         }
        }
    }
}
