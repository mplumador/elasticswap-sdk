<a id="LocalStorageAdapter"></a>

## <h5 style="margin: 10px 0px; border-width: 5px 0px; padding: 5px; border-style: solid;">LocalStorageAdapter ⇐ [`StorageAdapter`](#StorageAdapter)</h5>
**Kind**: global class  
**Extends**: [`StorageAdapter`](#StorageAdapter)  
<a id="new_LocalStorageAdapter_new"></a>

### <h5 style="margin: 10px 0px; border-width: 5px 0px; padding: 5px; border-style: solid;">new LocalStorageAdapter()</h5>
Provides a StorageAdapter implementation that uses the browser's local storage.

<a id="StorageAdapter"></a>

## <h5 style="margin: 10px 0px; border-width: 5px 0px; padding: 5px; border-style: solid;">StorageAdapter</h5>
**Kind**: global class  
<a id="new_StorageAdapter_new"></a>

### <h5 style="margin: 10px 0px; border-width: 5px 0px; padding: 5px; border-style: solid;">new StorageAdapter()</h5>
An abstract base class for storage adapters. These adapters are used by the Cache class tostore loaded blockchain data. The only reason to build one of these is to persist cached data tosome store type other than localStorage. By default the LocalStorageAdapter class is used.

<a id="ExchangeFactory"></a>

## <h5 style="margin: 10px 0px; border-width: 5px 0px; padding: 5px; border-style: solid;">ExchangeFactory ⇐ `Cachable`</h5>
**Kind**: global class  
**Extends**: `Cachable`  
<a id="new_ExchangeFactory_new"></a>

### <h5 style="margin: 10px 0px; border-width: 5px 0px; padding: 5px; border-style: solid;">new ExchangeFactory()</h5>
Provides a wrapping interface for the ExchangeFactory contract.

<a id="SDK"></a>

## <h5 style="margin: 10px 0px; border-width: 5px 0px; padding: 5px; border-style: solid;">SDK ⇐ `Subscribable`</h5>
**Kind**: global class  
**Extends**: `Subscribable`  

* [SDK](#SDK) ⇐ `Subscribable`
    * [new SDK()](#new_SDK_new)
    * [.SDK(config)](#SDK.SDK)

<a id="new_SDK_new"></a>

### <h5 style="margin: 10px 0px; border-width: 5px 0px; padding: 5px; border-style: solid;">new SDK()</h5>
Primary class. All things extend from here. SDK proxies ethers.js to provide an interface forall ElasticSwap EVM contracts.

<a id="SDK.SDK"></a>

### <h5 style="margin: 10px 0px; border-width: 5px 0px; padding: 5px; border-style: solid;">SDK.SDK(config)</h5>
Creates an instance of SDK.

**Kind**: static method of [`SDK`](#SDK)  
**See**

- [https://developer.mozilla.org/en-US/docs/Web/API/Fetch_API](https://developer.mozilla.org/en-US/docs/Web/API/Fetch_API)
- [https://docs.blocknative.com/notify#initialization](https://docs.blocknative.com/notify#initialization)
- [https://www.npmjs.com/package/hardhat-deploy/v/0.10.4#exporting-deployments](https://www.npmjs.com/package/hardhat-deploy/v/0.10.4#exporting-deployments)
- [https://docs.ethers.io/v5/api/providers/provider/](https://docs.ethers.io/v5/api/providers/provider/)
- [https://docs.ethers.io/v5/api/signer/](https://docs.ethers.io/v5/api/signer/)
- [StorageAdapter](#StorageAdapter)


| Param | Type | Description |
| --- | --- | --- |
| config | `Object` | { customFetch, env, provider, signer, storageAdapter } |
| config.customFetch | `function` | should implement the Fetch API (optional) |
| config.env | `Object` | environment configuration |
| config.env.blocknative | `Object` | bnc-notify initialization options |
| config.env.contracts | `Object` | deployed contract configuration by network |
| config.env.contracts[chainIdHex | `hardhat-deploy.Export` |  |
| config.env.deployments | `hardhat-deploy.MultiExport` | deployed contract configuration |
| config.provider | `ethers.providers.Provider` | default provider (optional) |
| config.signer | `ethers.Signer` | initial ethers signer (optional) |
| config.storageAdapter | [`StorageAdapter`](#StorageAdapter) | (optional) |

<a id="Multicall"></a>

## <h5 style="margin: 10px 0px; border-width: 5px 0px; padding: 5px; border-style: solid;">Multicall ⇐ `Base`</h5>
**Kind**: global class  
**Extends**: `Base`  
<a id="new_Multicall_new"></a>

### <h5 style="margin: 10px 0px; border-width: 5px 0px; padding: 5px; border-style: solid;">new Multicall()</h5>
A lightweight wrapper for ethers-multicall which allows for collection of many requestsTODO: Fork ethers-multicall and have it support multicall2

<a id="StakingPools"></a>

## <h5 style="margin: 10px 0px; border-width: 5px 0px; padding: 5px; border-style: solid;">StakingPools ⇐ `Base`</h5>
**Kind**: global class  
**Extends**: `Base`  

* [StakingPools](#StakingPools) ⇐ `Base`
    * [new StakingPools()](#new_StakingPools_new)
    * [.StakingPools(sdk, address)](#StakingPools.StakingPools)

<a id="new_StakingPools_new"></a>

### <h5 style="margin: 10px 0px; border-width: 5px 0px; padding: 5px; border-style: solid;">new StakingPools()</h5>
Provides a wrapping class for the StakingPools contract.

<a id="StakingPools.StakingPools"></a>

### <h5 style="margin: 10px 0px; border-width: 5px 0px; padding: 5px; border-style: solid;">StakingPools.StakingPools(sdk, address)</h5>
Creates an instance of StakingPools.

**Kind**: static method of [`StakingPools`](#StakingPools)  
**See**: [SDK#stakingPools](SDK#stakingPools)  

| Param | Type | Description |
| --- | --- | --- |
| sdk | [`SDK`](#SDK) | An instance of [SDK](#SDK) |
| address | `string` | An EVM compatible address of the contract. |

<a id="ERC20"></a>

## <h5 style="margin: 10px 0px; border-width: 5px 0px; padding: 5px; border-style: solid;">ERC20 ⇐ `Base`</h5>
**Kind**: global class  
**Extends**: `Base`  
<a id="new_ERC20_new"></a>

### <h5 style="margin: 10px 0px; border-width: 5px 0px; padding: 5px; border-style: solid;">new ERC20()</h5>
An ERC20 wrapper class that tracks any data requested and returns the cached version.

<a id="Token"></a>

## <h5 style="margin: 10px 0px; border-width: 5px 0px; padding: 5px; border-style: solid;">Token ⇐ [`ERC20`](#ERC20)</h5>
**Kind**: global class  
**Extends**: [`ERC20`](#ERC20)  
<a id="new_Token_new"></a>

### <h5 style="margin: 10px 0px; border-width: 5px 0px; padding: 5px; border-style: solid;">new Token()</h5>
Provides a wrapped for the ERC20 class that returns everything expected to be in a tokenlisttoken record while also providing ERC20 contract functionality.

<a id="TokenList"></a>

## <h5 style="margin: 10px 0px; border-width: 5px 0px; padding: 5px; border-style: solid;">TokenList ⇐ `Base`</h5>
**Kind**: global class  
**Extends**: `Base`  
<a id="new_TokenList_new"></a>

### <h5 style="margin: 10px 0px; border-width: 5px 0px; padding: 5px; border-style: solid;">new TokenList()</h5>
A wrapper class for token lists that links into the ERC20 contract class

<a id="TokensByAddress"></a>

## <h5 style="margin: 10px 0px; border-width: 5px 0px; padding: 5px; border-style: solid;">TokensByAddress ⇐ `Base`</h5>
**Kind**: global class  
**Extends**: `Base`  
<a id="new_TokensByAddress_new"></a>

### <h5 style="margin: 10px 0px; border-width: 5px 0px; padding: 5px; border-style: solid;">new TokensByAddress()</h5>
This class provides a simple way to access all tokens currently loaded in tokenlists by address.

<a id="areArraysEqual"></a>

## <h5 style="margin: 10px 0px; border-width: 5px 0px; padding: 5px; border-style: solid;">areArraysEqual ⇒ `boolean`</h5>
Compares two Objects, returning true if they are equal

**Kind**: global variable  
<a id="areObjectsEqual"></a>

## <h5 style="margin: 10px 0px; border-width: 5px 0px; padding: 5px; border-style: solid;">areObjectsEqual ⇒ `boolean`</h5>
Compares two functions, returning true if they are equal

**Kind**: global variable  
<a id="areFunctionsEqual"></a>

## <h5 style="margin: 10px 0px; border-width: 5px 0px; padding: 5px; border-style: solid;">areFunctionsEqual ⇒ `boolean`</h5>
Compares if the objects are exactly equal

**Kind**: global variable  
<a id="BASIS_POINTS"></a>

## <h5 style="margin: 10px 0px; border-width: 5px 0px; padding: 5px; border-style: solid;">BASIS\_POINTS ⇒ [`LiquidityQtyPairing`](#LiquidityQtyPairing)</h5>
**Kind**: global variable  
**Returns**: [`LiquidityQtyPairing`](#LiquidityQtyPairing) - baseTokenQty - qty of base token the user must supplyliquidityTokenQty - qty of liquidity tokens to be issued in exchange  
**Dev**: used to calculate the qty of base tokens required and liquiditytokens (deltaRo) to be issuedin order to add liquidity and remove base token decay.  

| Param | Description |
| --- | --- |
| baseTokenQtyDesired | the amount of base token the user wants to contribute |
| baseTokenQtyMin | the minimum amount of base token the user wants to contribute (allows for slippage) |
| baseTokenReserveQty | the external base token reserve qty prior to this transaction |
| totalSupplyOfLiquidityTokens | the total supply of our exchange's liquidity tokens (aka Ro) |
| internalBalances | internal balances struct from our exchange's internal accounting |

<a id="calculateAddBaseTokenLiquidityQuantities"></a>

## <h5 style="margin: 10px 0px; border-width: 5px 0px; padding: 5px; border-style: solid;">calculateAddBaseTokenLiquidityQuantities ⇒ [`LiquidityQtyPairing`](#LiquidityQtyPairing)</h5>
**Kind**: global variable  
**Returns**: [`LiquidityQtyPairing`](#LiquidityQtyPairing) - quoteTokenQty - qty of quote token the user must supplyliquidityTokenQty -  qty of liquidity tokens to be issued in exchange  
**Dev**: used to calculate the qty of quote token required and liquidity tokens (deltaRo)to be issuedin order to add liquidity and remove base token decay.  

| Param | Description |
| --- | --- |
| quoteTokenQtyDesired | the amount of quote token the user wants to contribute |
| quoteTokenQtyMin | the minimum amount of quote token the user wants to contribute (allows for slippage) |
| baseTokenReserveQty | the external base token reserve qty prior to this transaction |
| totalSupplyOfLiquidityTokens | the total supply of our exchange's liquidity tokens (aka Ro) |
| internalBalances | internal balances struct from our exchange's internal accounting |

<a id="calculateAddQuoteTokenLiquidityQuantities"></a>

## <h5 style="margin: 10px 0px; border-width: 5px 0px; padding: 5px; border-style: solid;">calculateAddQuoteTokenLiquidityQuantities ⇒</h5>
**Kind**: global variable  
**Returns**: baseTokenQty qty of base token the user must supplyquoteTokenQty qty of quote token the user must supplyliquidityTokenQty qty of liquidity tokens to be issued in exchange  
**Dev**: calculates the qty of base and quote tokens required and liquidity tokens (deltaRo)to be issuedin order to add liquidity when no decay is present.  

| Param | Description |
| --- | --- |
| baseTokenQtyDesired | the amount of base token the user wants to contribute |
| quoteTokenQtyDesired | the amount of quote token the user wants to contribute |
| baseTokenQtyMin | the minimum amount of base token the user wants to contribute (allows for slippage) |
| quoteTokenQtyMin | the minimum amount of quote token the user wants to contribute (allows for slippage) |
| quoteTokenReserveQty | the external quote token reserve qty prior to this transaction |
| totalSupplyOfLiquidityTokens | the total supply of our exchange's liquidity tokens (aka Ro) |
| internalBalances | internal balances struct from our exchange's internal accounting |

<a id="calculateAddTokenPairLiquidityQuantities"></a>

## <h5 style="margin: 10px 0px; border-width: 5px 0px; padding: 5px; border-style: solid;">calculateAddTokenPairLiquidityQuantities ⇒</h5>
**Kind**: global variable  
**Returns**: baseTokenQty qty of base token the user will receive back  
**Dev**: calculates the qty of base tokens a user will receive for swapping their quotetokens (less fees)  

| Param | Description |
| --- | --- |
| quoteTokenQty | the amount of quote tokens the user wants to swap |
| baseTokenQtyMin | the minimum about of base tokens they are willing to receive in return (slippage) |
| baseTokenReserveQty | the external base token reserve qty prior to this transaction |
| liquidityFeeInBasisPoints | the current total liquidity fee represented as an integer of basis points |
| internalBalances | internal balances struct from our exchange's internal accounting |

<a id="calculateBaseTokenQty"></a>

## <h5 style="margin: 10px 0px; border-width: 5px 0px; padding: 5px; border-style: solid;">calculateBaseTokenQty ⇒</h5>
**Kind**: global variable  
**Returns**: exchangeRate - the current exchange rate  
**Dev**: calculates the current exchange rate (X/Y)  

| Param | Description |
| --- | --- |
| inputTokenReserveQty | The reserve qty of the X token (the baseToken) (the elastic token, in an elastic pair) |
| outputTokenReserveQty | The reserve qty of the Y token (the quoteToken) (the non-elastic token, in an elastic pair) |

<a id="calculateExchangeRate"></a>

## <h5 style="margin: 10px 0px; border-width: 5px 0px; padding: 5px; border-style: solid;">calculateExchangeRate ⇒</h5>
**Kind**: global variable  
**Returns**: fees - the fee amount  
**Dev**: calculates the fees  

| Param | Description |
| --- | --- |
| feesInBasisPoints | the amount of fees in basis points |
| swapAmount | the amount being traded |

<a id="calculateFees"></a>

## <h5 style="margin: 10px 0px; border-width: 5px 0px; padding: 5px; border-style: solid;">calculateFees ⇒</h5>
**Kind**: global variable  
**Returns**: inputAmountFromOutputAmount  
**Dev**: calculates the inputAmount given an OutputAmountinputAmount =  - (outputAmount * inputTokenReserveQty * BASIS_POINTS)               -----------------------------------------------------------------               ( outputAmount - outputTokenReserveQty + (outputTokenReserveQty* (slippage/100)) )                 * (BP - liquidityFeeInBasisPoints )  

| Param | Description |
| --- | --- |
| outputTokenAmount | The amount user wants to receive after fees and slippage |
| inputTokenReserveQty | The reserve quantity of the inputToken |
| outputTokenReserveQty | The reserve quantity of the output |
| slippagePercent | The percentage of the slippage |
| liquidityFeeInBasisPoints | The liquidity fee in BasisPoints |

<a id="calculateInputAmountFromOutputAmount"></a>

## <h5 style="margin: 10px 0px; border-width: 5px 0px; padding: 5px; border-style: solid;">calculateInputAmountFromOutputAmount ⇒</h5>
**Kind**: global variable  
**Returns**: liquidityTokenQty qty of liquidity tokens to be issued in exchange  
**Dev**: used to calculate the qty of liquidity tokens (deltaRo) we will be issued to a supplierof a single asset entry when decay is present.  

| Param | Description |
| --- | --- |
| totalSupplyOfLiquidityTokens | the total supply of our exchange's liquidity tokens (aka Ro) |
| quoteTokenQty | the amount of quote token the user it adding to the pool (deltaB or deltaY) |
| quoteTokenReserveBalance | the total balance (external) of quote tokens in our pool (Beta) |

<a id="calculateLiquidityTokenQtyForDoubleAssetEntry"></a>

## <h5 style="margin: 10px 0px; border-width: 5px 0px; padding: 5px; border-style: solid;">calculateLiquidityTokenQtyForDoubleAssetEntry ⇒</h5>
**Kind**: global variable  
**Returns**: liquidityTokenQty qty of liquidity tokens to be issued in exchange  
**Dev**: used to calculate the qty of liquidity tokens (deltaRo) we will be issued to a supplierof a single asset entry when decay is present.  

| Param | Description |
| --- | --- |
| totalSupplyOfLiquidityTokens | the total supply of our exchange's liquidity tokens (aka Ro) |
| tokenQtyAToAdd | the amount of tokens being added by the caller to remove the current decay |
| internalTokenAReserveQty | the internal balance (X or Y) of token A as a result of this transaction |
| tokenBDecayChange | the change that will occur in the decay in the opposite token as a result of this transaction |
| tokenBDecay | the amount of decay in tokenB |

<a id="calculateLiquidityTokenQtyForSingleAssetEntry"></a>

## <h5 style="margin: 10px 0px; border-width: 5px 0px; padding: 5px; border-style: solid;">calculateLiquidityTokenQtyForSingleAssetEntry ⇒</h5>
**Kind**: global variable  
**Returns**: outputAmountLessSlippage  
**Dev**: calculates the min amount of output tokens given the slippage percent supplied  

| Param | Description |
| --- | --- |
| inputTokenAmount | base or quote token qty to be swapped by the trader |
| inputTokenReserveQty | current reserve qty of the base or quote token (same token as tokenA) |
| outputTokenReserveQty | current reserve qty of the other base or quote token (not tokenA) |
| slippagePercent | the percentage of slippage |
| feeAmount | the total amount of fees in Basis points for the trade |

<a id="calculateOutputAmountLessFees"></a>

## <h5 style="margin: 10px 0px; border-width: 5px 0px; padding: 5px; border-style: solid;">calculateOutputAmountLessFees ⇒</h5>
**Kind**: global variable  
**Returns**: tokenBQty  
**Dev**: used to calculate the qty of token a liquidity providermust add in order to maintain the current reserve ratios  

| Param | Description |
| --- | --- |
| tokenAQty | base or quote token qty to be supplied by the liquidity provider |
| tokenAReserveQty | current reserve qty of the base or quote token (same token as tokenA) |
| tokenBReserveQty | current reserve qty of the other base or quote token (not tokenA) |

<a id="calculateQty"></a>

## <h5 style="margin: 10px 0px; border-width: 5px 0px; padding: 5px; border-style: solid;">calculateQty ⇒</h5>
**Kind**: global variable  
**Returns**: qtyToReturn  
**Dev**: used to calculate the qty of token a trader will receive (less fees)given the qty of token A they are providing  

| Param | Description |
| --- | --- |
| tokenASwapQty | base or quote token qty to be swapped by the trader |
| tokenAReserveQty | current reserve qty of the base or quote token (same token as tokenA) |
| tokenBReserveQty | current reserve qty of the other base or quote token (not tokenA) |
| liquidityFeeInBasisPoints | fee to liquidity providers represented in basis points |

<a id="calculateQtyToReturnAfterFees"></a>

## <h5 style="margin: 10px 0px; border-width: 5px 0px; padding: 5px; border-style: solid;">calculateQtyToReturnAfterFees ⇒</h5>
**Kind**: global variable  
**Returns**: quoteTokenQty qty of quote token the user will receive back  
**Dev**: calculates the qty of quote tokens a user will receive for swapping their basetokens (less fees)  

| Param | Description |
| --- | --- |
| baseTokenQty | the amount of bases tokens the user wants to swap |
| quoteTokenQtyMin | the minimum about of quote tokens they are willing to receive in return (slippage) |
| liquidityFeeInBasisPoints | the current total liquidity fee represented as an integer of basis points |
| internalBalances | internal balances struct from our exchange's internal accounting |

<a id="calculateQuoteTokenQty"></a>

## <h5 style="margin: 10px 0px; border-width: 5px 0px; padding: 5px; border-style: solid;">calculateQuoteTokenQty ⇒ [`LiquidityQtyPairing`](#LiquidityQtyPairing)</h5>
**Kind**: global variable  
**Returns**: [`LiquidityQtyPairing`](#LiquidityQtyPairing) - tokenAmounts - The min amounts of each token received byredeeming @param lpTokenQtyToRedeemMath: (not accounting for slippage)ΔX = α * ΔRo / RoΔY = β * ΔRo / Rowhere,# ΔRo - The amount of liquidity tokens the liquidity provider wants to exchange# ΔX - The amount of baseToken the liquidity provider receives# ΔY - The amount of quoteTokens the liquidity provider receives# α - The balance of baseToken currently in the exchange# β - The balance of quoteToken currently in the exchangeAccounting for slippage:quoteTokenReceived = deltaX * (1 - (slippage/percent))baseTokenReceived = deltaY *  (1 - (slippage/percent))  
**Dev**: returns the min amount of each token received by redeeming @param lpTokenQtyToRedeem  

| Param | Description |
| --- | --- |
| lpTokenQtyToRedeem | the amount of LP tokens user wants to redeem |
| slippagePercent | the percentage of slippage set by the user |
| baseTokenReserveQty | current reserve qty of the base token (the Elastic token if it is an elastic pair) |
| quoteTokenReserveQty | current reserve qty of the quote token (the non-Elastic token if it is an elastic pair) |
| totalLPTokenSupply | current total outstanding qty of the LP token |

<a id="calculateTokenAmountsFromLPTokens"></a>

## <h5 style="margin: 10px 0px; border-width: 5px 0px; padding: 5px; border-style: solid;">calculateTokenAmountsFromLPTokens</h5>
**Kind**: global variable  
**Dev**: defines the amount of decay needed in order for us to require a user to handle thedecay prior to a double asset entry as the equivalent of 1 unit of quote token  

| Param | Type | Description |
| --- | --- | --- |
| baseTokenReserveQty |  | current reserve qty of the baseToken |
| internalBalances | [`internalBalances`](#internalBalances) | the internal balance Struct internalBalances = |

<a id="validate"></a>

## <h5 style="margin: 10px 0px; border-width: 5px 0px; padding: 5px; border-style: solid;">validate ⇒ `boolean`</h5>
validates that thing is an Array

**Kind**: global variable  

| Param | Type | Description |
| --- | --- | --- |
| thing | `\*` | the thing to validate |
| options | `Object` | @see [validate](#validate) |

<a id="validateIsArray"></a>

## <h5 style="margin: 10px 0px; border-width: 5px 0px; padding: 5px; border-style: solid;">validateIsArray ⇒ `boolean`</h5>
validates that thing is a MikeMCL BigNumber

**Kind**: global variable  

| Param | Type | Description |
| --- | --- | --- |
| thing | `\*` | the thing to validate |
| options | `Object` | @see [validate](#validate) |

<a id="validateIsBigNumber"></a>

## <h5 style="margin: 10px 0px; border-width: 5px 0px; padding: 5px; border-style: solid;">validateIsBigNumber ⇒ `boolean`</h5>
validates that thing is a Date

**Kind**: global variable  

| Param | Type | Description |
| --- | --- | --- |
| thing | `\*` | the thing to validate |
| options | `Object` | @see [validate](#validate) |

<a id="validateIsDate"></a>

## <h5 style="margin: 10px 0px; border-width: 5px 0px; padding: 5px; border-style: solid;">validateIsDate ⇒ `boolean`</h5>
validates that thing is a Function

**Kind**: global variable  

| Param | Type | Description |
| --- | --- | --- |
| thing | `\*` | the thing to validate |
| options | `Object` | @see [validate](#validate) |

<a id="validateIsFunction"></a>

## <h5 style="margin: 10px 0px; border-width: 5px 0px; padding: 5px; border-style: solid;">validateIsFunction ⇒ `boolean`</h5>
validates that thing is a Number

**Kind**: global variable  

| Param | Type | Description |
| --- | --- | --- |
| thing | `\*` | the thing to validate |
| options | `Object` | @see [validate](#validate) |

<a id="validateIsNumber"></a>

## <h5 style="margin: 10px 0px; border-width: 5px 0px; padding: 5px; border-style: solid;">validateIsNumber ⇒ `boolean`</h5>
validates that thing is a plain Object

**Kind**: global variable  

| Param | Type | Description |
| --- | --- | --- |
| thing | `\*` | the thing to validate |
| options | `Object` | @see [validate](#validate) |

<a id="validateIsPOJO"></a>

## <h5 style="margin: 10px 0px; border-width: 5px 0px; padding: 5px; border-style: solid;">validateIsPOJO ⇒ `boolean`</h5>
validates that thing is a Set

**Kind**: global variable  

| Param | Type | Description |
| --- | --- | --- |
| thing | `\*` | the thing to validate |
| options | `Object` | @see [validate](#validate) |

<a id="validateIsSet"></a>

## <h5 style="margin: 10px 0px; border-width: 5px 0px; padding: 5px; border-style: solid;">validateIsSet ⇒ `boolean`</h5>
validates that thing is a String

**Kind**: global variable  

| Param | Type | Description |
| --- | --- | --- |
| thing | `\*` | the thing to validate |
| options | `Object` | @see [validate](#validate) |

<a id="validateIsString"></a>

## <h5 style="margin: 10px 0px; border-width: 5px 0px; padding: 5px; border-style: solid;">validateIsString ⇒ `boolean`</h5>
validates that thing is an EVM address

**Kind**: global variable  

| Param | Type | Description |
| --- | --- | --- |
| thing | `\*` | the thing to validate |
| options | `Object` | @see [validate](#validate) |

<a id="validateIsAddress"></a>

## <h5 style="margin: 10px 0px; border-width: 5px 0px; padding: 5px; border-style: solid;">validateIsAddress ⇒ `boolean`</h5>
validates that thing is an EVM transaction hash

**Kind**: global variable  

| Param | Type | Description |
| --- | --- | --- |
| thing | `\*` | the thing to validate |
| options | `Object` | @see [validate](#validate) |

<a id="getType"></a>

## <h5 style="margin: 10px 0px; border-width: 5px 0px; padding: 5px; border-style: solid;">getType(obj) ⇒ `String`</h5>
More accurately check the type of a JavaScript object

**Kind**: global function  
**Returns**: `String` - The object type  

| Param | Type | Description |
| --- | --- | --- |
| obj | `Object` | The object |

<a id="areArraysEqual"></a>

## <h5 style="margin: 10px 0px; border-width: 5px 0px; padding: 5px; border-style: solid;">areArraysEqual() ⇒ `boolean`</h5>
Compares two arrays and returns true if they are equal

**Kind**: global function  
<a id="buildError"></a>

## <h5 style="margin: 10px 0px; border-width: 5px 0px; padding: 5px; border-style: solid;">buildError(options) ⇒ `string`</h5>
Returns a formatted error message for use with throw

**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| options | `Object` | { message, prefix } |
| options.message | `string` | the message |
| options.prefix | `string` | the prefix, default is '@elasticswap/sdk - validations' |

<a id="validate"></a>

## <h5 style="margin: 10px 0px; border-width: 5px 0px; padding: 5px; border-style: solid;">validate(options) ⇒ `boolean`</h5>
returns true if the result is truthy or throws a TypeError as specified by options

**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| options | `Object` | { level, message, prefix, throwError = true } |
| options.level | `string` | the name of the console function to use, default is 'error' |
| options.message | `string` | the error message in case result is false |
| options.prefix | `string` | the prefix, default is '@elasticswap/sdk - validations' |

<a id="LiquidityQtyPairing"></a>

## <h5 style="margin: 10px 0px; border-width: 5px 0px; padding: 5px; border-style: solid;">LiquidityQtyPairing : `Object`</h5>
**Kind**: global typedef  
**Properties**

| Name | Type |
| --- | --- |
| otherTokenQty | `BigNumber` | 
| liquidityTokenQty | `BigNumber` | 

<a id="internalBalances"></a>

## <h5 style="margin: 10px 0px; border-width: 5px 0px; padding: 5px; border-style: solid;">internalBalances : `Object`</h5>
**Kind**: global typedef  
**Properties**

| Name | Type |
| --- | --- |
| baseTokenReserveQty | `BigNumber` | 
| quoteTokenReserveQTY | `BigNumber` | 

