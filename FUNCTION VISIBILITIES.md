                                                       TOPIC 1: FUNCTION VISIBILITY 
When developing smart contract, you must pay attention to some important aspects in order to be able to develop efficient code. The programing language we are going to use as reference is solidity (the most popular programing languages in the blockchain space) 

In this topic we are going to talk about public, external, internal and private visibility keywords generally assigned to functions when writing smart contract. But we will pinpoint the major difference between Public and external visibility.
Basically, we can state that: 
๐๐ฎ๐๐ฅ๐ข๐ ๐๐ฎ๐ง๐๐ญ๐ข๐จ๐ง: Can be called from everywhere, internally as well as from outside the Contract. Moreover, Public function leads to higher gas costs.

๐๐ฑ๐ญ๐๐ซ๐ง๐๐ฅ ๐๐ฎ๐ง๐๐ญ๐ข๐จ๐ง: Can only be called from outside the contract and not accessible from within the contract. Compeer to public function, External function Costs Comparatively Lower GAS.
Internal Function: can only be accessed from within the current contract or contracts deriving from it. They cannot be accessed externally. Since they are not exposed to the outside through the contractโs ABI, they can take parameters of internal types like mappings or storage references.
Private Function: is like internal but it is not visible in derived contracts.


๐ต๐๐, it is important to know why public function costs higher gas price comper to external function

In the case of PUBLIC Functions, arguments of the Functions are copied into ๐๐๐๐๐๐.
While on the other hand, Functions with External visibility can directly read arguments from ๐๐๐๐๐๐๐๐.

๐๐๐ฃ๐๐ ๐พ๐ผ๐๐๐ฟ๐ผ๐๐ผ ๐๐จ ๐พ๐๐๐ผ๐๐๐ ๐ฉ๐๐๐ฃ ๐๐๐๐๐๐, ๐๐ญ๐ฉ๐๐ง๐ฃ๐๐ก ๐๐ช๐ฃ๐๐ฉ๐๐ค๐ฃ๐จ ๐ง๐๐จ๐ช๐ก๐ฉ ๐๐ฃ ๐ ๐ก๐ค๐ฌ๐๐ง ๐๐ญ๐๐๐ช๐ฉ๐๐ค๐ฃ ๐พ๐ค๐จ๐ฉ(๐๐๐จ) ๐ฉ๐๐๐ฃ ๐๐๐ฝ๐๐๐พ ๐๐ช๐ฃ๐๐ฉ๐๐ค๐ฃ๐จ.

โข	NB: Now what most people donโt know is that External function can also be called inside the contract but you lose all the benefits of gas savings. To do so just type โthis.ExternalFunction();โ
โข	Making something private or internal only prevents others contracts from reading or modifying the information but it will still be visible to the whole world outside of the blockchain.


