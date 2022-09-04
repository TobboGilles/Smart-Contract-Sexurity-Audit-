                                          TOPIC 2: Default Visibility 


Functions in Solidity have visibility specifiers which dictate how functions are allowed to be called. The visibility determines whether a function can be called externally by users, by other derived smart contracts, only internally or only externally. There are four visibility specifiers, which are described in detail in the Topic 1 “FUNCTION VISIBILITY” that I wrote earlier before. Note that All Functions are to set public by default allowing users to call them externally. Incorrect use of visibility specifiers can lead to some devastating vulnerabilities in smart contracts as will be discussed in this topic.

The Vulnerability
The default visibility for functions is public. Therefore, functions that do not specify any visibility will be callable by external users. The issue comes when developers mistakenly ignore visibility specifiers on functions which should be private (or only callable within the contract itself).

Let's analyze this piece of code to have a clear understanding of the vulnerability. See the picture bellow.
 
This contract is designed to act as an address guessing bounty game. To win the balance of the contract, a user must generate an Ethereum address whose last 8 hex characters are 0. Once condition respected, they can call the WithdrawWinnings() function to obtain their bounty.
Unfortunately, the visibility of the functions has not been specified. In particular, the _sendWinnings() function is public and thus any address can call this function to steal the bounty.


How to prevent it:
It is good practice to always specify the visibility of all functions in a contract, even if they are intentionally public. Recent versions of Solidity will now show warnings during compilation for functions that have no explicit visibility set, to help encourage this practice.

