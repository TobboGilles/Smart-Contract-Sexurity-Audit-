                                                       TOPIC 1: FUNCTION VISIBILITY 
When developing smart contract, you must pay attention to some important aspects in order to be able to develop efficient code. The programing language we are going to use as reference is solidity (the most popular programing languages in the blockchain space) 

In this topic we are going to talk about public, external, internal and private visibility keywords generally assigned to functions when writing smart contract. But we will pinpoint the major difference between Public and external visibility.
Basically, we can state that: 
𝐏𝐮𝐛𝐥𝐢𝐜 𝐅𝐮𝐧𝐜𝐭𝐢𝐨𝐧: Can be called from everywhere, internally as well as from outside the Contract. Moreover, Public function leads to higher gas costs.

𝐄𝐱𝐭𝐞𝐫𝐧𝐚𝐥 𝐅𝐮𝐧𝐜𝐭𝐢𝐨𝐧: Can only be called from outside the contract and not accessible from within the contract. Compeer to public function, External function Costs Comparatively Lower GAS.
Internal Function: can only be accessed from within the current contract or contracts deriving from it. They cannot be accessed externally. Since they are not exposed to the outside through the contract’s ABI, they can take parameters of internal types like mappings or storage references.
Private Function: is like internal but it is not visible in derived contracts.


𝑵𝒐𝒘, it is important to know why public function costs higher gas price comper to external function

In the case of PUBLIC Functions, arguments of the Functions are copied into 𝐌𝐄𝐌𝐎𝐑𝐘.
While on the other hand, Functions with External visibility can directly read arguments from 𝐂𝐀𝐋𝐋𝐃𝐀𝐓𝐀.

𝙎𝙞𝙣𝙘𝙚 𝘾𝘼𝙇𝙇𝘿𝘼𝙏𝘼 𝙞𝙨 𝘾𝙃𝙀𝘼𝙋𝙀𝙍 𝙩𝙝𝙖𝙣 𝙈𝙀𝙈𝙊𝙍𝙔, 𝙀𝙭𝙩𝙚𝙧𝙣𝙖𝙡 𝙁𝙪𝙣𝙘𝙩𝙞𝙤𝙣𝙨 𝙧𝙚𝙨𝙪𝙡𝙩 𝙞𝙣 𝙖 𝙡𝙤𝙬𝙚𝙧 𝙀𝙭𝙚𝙘𝙪𝙩𝙞𝙤𝙣 𝘾𝙤𝙨𝙩(𝙂𝙖𝙨) 𝙩𝙝𝙖𝙣 𝙋𝙐𝘽𝙇𝙄𝘾 𝙁𝙪𝙣𝙘𝙩𝙞𝙤𝙣𝙨.

•	NB: Now what most people don’t know is that External function can also be called inside the contract but you lose all the benefits of gas savings. To do so just type “this.ExternalFunction();”
•	Making something private or internal only prevents others contracts from reading or modifying the information but it will still be visible to the whole world outside of the blockchain.


