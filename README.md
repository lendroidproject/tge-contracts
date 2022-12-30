How to withdraw your vested LST

1. Select the contract
To directly interact with the vesting smart contracts, you will need the following two items.

1.1. Contract ABI
This can be obtained from here.

1.2. Contract address
This needs to be one of the following addresses

i. 0xC25A27281e10f140A97EA5f845c0De1BF8782f90

ii. 0xE1A2D917931b0E88bd38f69D4E31e94a32986481

iii. 0xa9261e36bD84382B56154fB4ed4C93313bB26EFe

iv. 0x581db4a90d530CdE51E40a055528070e006B22C1

v. 0x0ff676a8d4698b21151fc87680f6479209da8770

vi. 0xc3253f20821403f6d0b54c060179123dec47b07e

vii. 0x547bf920515464c98a84777d2ad8eb94be55a532

viii. 0xb69192d92d1a3bcc7e840350449d4f1c89e6248f

ix. 0x3ff911a6b29d13a3b499bc11cae12aadfbdaa0c1

You can now get the contract using its address and ABI.

For eg, using ethersjs, you can get the distribution contract as below.

distributionContract = new ethers.Contract(address, abi)

where address and abi can be obtained from 2 and 1 above respectively.

2. Choose the contract function
2.1. To check the LST allocated to your ETH address
You can check your allocations by calling the function allocations(YOUR_ETH_ADDRESS_HERE). The corresponding hash of the function is 52a9039c.

2.2. If you have never withdrawn your allocated LST previously
Follow step 1 above to see if your allocation details indicate whether you have vested or not.

2.2.1 If your LST was not vested
You can withdraw 100% of your allocated LST by calling the function withdraw(). The corresponding hash of the function is 0x3ccfd60b.

2.2.2 If your LST was vested
Follow step 2.2.1 to withdraw 10% of your allocated LST.

Then proceed to step 2.3 to withdraw the remaining 90% of your allocated LST.

2.3. If you have already withdrawn a portion of your vested LST
You can withdraw the remaining LST by calling the function releaseVestedTokens(YOUR_ETH_ADDRESS_HERE). The corresponding hash of the function is 0xce699a41.
