[Vault client for node.js](../README.md) › [Globals](../globals.md) › [InitSysBackend](initsysbackend.md)

# Class: InitSysBackend

## Hierarchy

  ↳ [BaseSysBackend](basesysbackend.md)

  ↳ **InitSysBackend**

## Index

### Constructors

* [constructor](initsysbackend.md#constructor)

### Methods

* [readInitStatus](initsysbackend.md#readinitstatus)
* [startInit](initsysbackend.md#startinit)

## Constructors

###  constructor

\+ **new InitSysBackend**(`baseUrl`: [BaseUrl](../globals.md#baseurl), `authToken?`: [AuthTokenParam](../globals.md#authtokenparam)): *[InitSysBackend](initsysbackend.md)*

*Inherited from [BaseSysBackend](basesysbackend.md).[constructor](basesysbackend.md#constructor)*

*Overrides void*

*Defined in [system-backends/BaseSysBackend.ts:4](https://github.com/theogravity/vault-tacular/blob/a3c7591/src/system-backends/BaseSysBackend.ts#L4)*

**Parameters:**

Name | Type | Description |
------ | ------ | ------ |
`baseUrl` | [BaseUrl](../globals.md#baseurl) | The URL to the Vault API including the version path |
`authToken?` | [AuthTokenParam](../globals.md#authtokenparam) | - |

**Returns:** *[InitSysBackend](initsysbackend.md)*

## Methods

###  readInitStatus

▸ **readInitStatus**(): *Promise‹[IVaultResponse](../interfaces/ivaultresponse.md)‹[IReadInitStatusResponse](../globals.md#ireadinitstatusresponse)››*

*Defined in [system-backends/InitSysBackend.ts:12](https://github.com/theogravity/vault-tacular/blob/a3c7591/src/system-backends/InitSysBackend.ts#L12)*

Returns the initialization status of Vault.

**`link`** https://www.vaultproject.io/api/system/init.html#read-initialization-status

**Returns:** *Promise‹[IVaultResponse](../interfaces/ivaultresponse.md)‹[IReadInitStatusResponse](../globals.md#ireadinitstatusresponse)››*

___

###  startInit

▸ **startInit**(`payload`: [IStartInitPayload](../globals.md#istartinitpayload), `enterprisePayload?`: [IStartInitEntPayload](../globals.md#istartinitentpayload)): *Promise‹[IVaultResponse](../interfaces/ivaultresponse.md)‹[IStartInitResponse](../globals.md#istartinitresponse)››*

*Defined in [system-backends/InitSysBackend.ts:29](https://github.com/theogravity/vault-tacular/blob/a3c7591/src/system-backends/InitSysBackend.ts#L29)*

Initializes a new Vault. The Vault must not have been previously initialized. The recovery
options, as well as the stored shares option, are only available when using Vault HSM.

**`link`** https://www.vaultproject.io/api/system/init.html#start-initialization

**Parameters:**

Name | Type |
------ | ------ |
`payload` | [IStartInitPayload](../globals.md#istartinitpayload) |
`enterprisePayload?` | [IStartInitEntPayload](../globals.md#istartinitentpayload) |

**Returns:** *Promise‹[IVaultResponse](../interfaces/ivaultresponse.md)‹[IStartInitResponse](../globals.md#istartinitresponse)››*
