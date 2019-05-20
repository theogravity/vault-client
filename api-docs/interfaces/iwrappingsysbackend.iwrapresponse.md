[Vault client for node.js](../README.md) > [IWrappingSysBackend](../modules/iwrappingsysbackend.md) > [IWrapResponse](../interfaces/iwrappingsysbackend.iwrapresponse.md)

# Interface: IWrapResponse

## Hierarchy

 [IUnwrapResponse](iwrappingsysbackend.iunwrapresponse.md)

**↳ IWrapResponse**

## Index

### Properties

* [data](iwrappingsysbackend.iwrapresponse.md#data)
* [lease_duration](iwrappingsysbackend.iwrapresponse.md#lease_duration)
* [lease_id](iwrappingsysbackend.iwrapresponse.md#lease_id)
* [renewable](iwrappingsysbackend.iwrapresponse.md#renewable)
* [request_id](iwrappingsysbackend.iwrapresponse.md#request_id)
* [warnings](iwrappingsysbackend.iwrapresponse.md#warnings)
* [wrap_info](iwrappingsysbackend.iwrapresponse.md#wrap_info)

---

## Properties

<a id="data"></a>

###  data

**● data**: *`object`*

*Inherited from [IUnwrapResponse](iwrappingsysbackend.iunwrapresponse.md).[data](iwrappingsysbackend.iunwrapresponse.md#data)*

*Defined in [interfaces/system-backend/IWrappingSysBackend.ts:30](https://github.com/theogravity/vault-client/blob/38077d0/src/interfaces/system-backend/IWrappingSysBackend.ts#L30)*

The set of parameters in the wrapped response from wrap().

#### Type declaration

[key: `string`]: `any`

___
<a id="lease_duration"></a>

###  lease_duration

**● lease_duration**: *`number`*

*Inherited from [IUnwrapResponse](iwrappingsysbackend.iunwrapresponse.md).[lease_duration](iwrappingsysbackend.iunwrapresponse.md#lease_duration)*

*Defined in [interfaces/system-backend/IWrappingSysBackend.ts:25](https://github.com/theogravity/vault-client/blob/38077d0/src/interfaces/system-backend/IWrappingSysBackend.ts#L25)*

___
<a id="lease_id"></a>

###  lease_id

**● lease_id**: *`string`*

*Inherited from [IUnwrapResponse](iwrappingsysbackend.iunwrapresponse.md).[lease_id](iwrappingsysbackend.iunwrapresponse.md#lease_id)*

*Defined in [interfaces/system-backend/IWrappingSysBackend.ts:24](https://github.com/theogravity/vault-client/blob/38077d0/src/interfaces/system-backend/IWrappingSysBackend.ts#L24)*

___
<a id="renewable"></a>

###  renewable

**● renewable**: *`boolean`*

*Inherited from [IUnwrapResponse](iwrappingsysbackend.iunwrapresponse.md).[renewable](iwrappingsysbackend.iunwrapresponse.md#renewable)*

*Defined in [interfaces/system-backend/IWrappingSysBackend.ts:26](https://github.com/theogravity/vault-client/blob/38077d0/src/interfaces/system-backend/IWrappingSysBackend.ts#L26)*

___
<a id="request_id"></a>

###  request_id

**● request_id**: *`string`*

*Inherited from [IUnwrapResponse](iwrappingsysbackend.iunwrapresponse.md).[request_id](iwrappingsysbackend.iunwrapresponse.md#request_id)*

*Defined in [interfaces/system-backend/IWrappingSysBackend.ts:23](https://github.com/theogravity/vault-client/blob/38077d0/src/interfaces/system-backend/IWrappingSysBackend.ts#L23)*

___
<a id="warnings"></a>

###  warnings

**● warnings**: *[VaultWarnings](../#vaultwarnings)*

*Inherited from [IUnwrapResponse](iwrappingsysbackend.iunwrapresponse.md).[warnings](iwrappingsysbackend.iunwrapresponse.md#warnings)*

*Defined in [interfaces/system-backend/IWrappingSysBackend.ts:33](https://github.com/theogravity/vault-client/blob/38077d0/src/interfaces/system-backend/IWrappingSysBackend.ts#L33)*

___
<a id="wrap_info"></a>

###  wrap_info

**● wrap_info**: *[IWrapInfo](iwrapinfo.md)*

*Defined in [interfaces/system-backend/IWrappingSysBackend.ts:44](https://github.com/theogravity/vault-client/blob/38077d0/src/interfaces/system-backend/IWrappingSysBackend.ts#L44)*

___
