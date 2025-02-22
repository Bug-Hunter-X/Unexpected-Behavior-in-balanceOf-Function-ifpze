# Unexpected Behavior in balanceOf Function

This repository demonstrates a common error in Dapps: failing to handle cases where a user has a zero balance.  The `balanceOf` function in `bug.sol` doesn't explicitly handle this, leading to potential issues.

The solution, found in `bugSolution.sol`, addresses this by explicitly returning 0 if the account has no balance.

## Steps to Reproduce

1. Compile `bug.sol`.
2. Deploy the contract.
3. Call `balanceOf` for an address that doesn't exist, or hasn't interacted with the contract. 
   You may observe unpredictable behavior depending on the EVM.

## Solution

The `bugSolution.sol` file shows a corrected version of the function that explicitly returns 0 when an account has no balance.