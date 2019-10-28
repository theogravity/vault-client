> **[Vault client for node.js](../README.md)**

[Globals](../globals.md) / [Kv1SecretEngine](kv1secretengine.md) /

# Class: Kv1SecretEngine

Vault KV secrets engine.

## Hierarchy

  * [BaseSecretEngine](basesecretengine.md)

  * **Kv1SecretEngine**

## Index

### Constructors

* [constructor](kv1secretengine.md#constructor)

### Methods

* [createOrUpdateSecret](kv1secretengine.md#createorupdatesecret)
* [deleteSecret](kv1secretengine.md#deletesecret)
* [listSecrets](kv1secretengine.md#listsecrets)
* [readSecret](kv1secretengine.md#readsecret)

## Constructors

###  constructor

\+ **new Kv1SecretEngine**(`baseUrl`: [BaseUrl](../globals.md#baseurl), `config?`: [IBaseClientConfig](../interfaces/ibaseclientconfig.md)): *[Kv1SecretEngine](kv1secretengine.md)*

*Defined in [secrets-engines/Kv1SecretEngine.ts:15](https://github.com/theogravity/vault-tacular/blob/68ec17c/src/secrets-engines/Kv1SecretEngine.ts#L15)*

**Parameters:**

Name | Type |
------ | ------ |
`baseUrl` | [BaseUrl](../globals.md#baseurl) |
`config?` | [IBaseClientConfig](../interfaces/ibaseclientconfig.md) |

**Returns:** *[Kv1SecretEngine](kv1secretengine.md)*

## Methods

###  createOrUpdateSecret

▸ **createOrUpdateSecret**(`path`: string, `payload`: [ICreateOrUpdateSecretPayload](../interfaces/ikv1secretengine.icreateorupdatesecretpayload.md)): *`Promise<IVaultResponse<void>>`*

*Defined in [secrets-engines/Kv1SecretEngine.ts:77](https://github.com/theogravity/vault-tacular/blob/68ec17c/src/secrets-engines/Kv1SecretEngine.ts#L77)*

Stores a secret at the specified location. If the value does not yet exist, the calling
token must have an ACL policy granting the create capability. If the value already exists,
the calling token must have an ACL policy granting the update capability.

**`link`** https://www.vaultproject.io/api/secret/kv/kv-v1.html#create-update-secret

**Parameters:**

Name | Type |
------ | ------ |
`path` | string |
`payload` | [ICreateOrUpdateSecretPayload](../interfaces/ikv1secretengine.icreateorupdatesecretpayload.md) |

**Returns:** *`Promise<IVaultResponse<void>>`*

___

###  deleteSecret

▸ **deleteSecret**(`path`: string): *`Promise<IVaultResponse<void>>`*

*Defined in [secrets-engines/Kv1SecretEngine.ts:99](https://github.com/theogravity/vault-tacular/blob/68ec17c/src/secrets-engines/Kv1SecretEngine.ts#L99)*

Deletes the secret at the specified location.

**`link`** https://www.vaultproject.io/api/secret/kv/kv-v1.html#delete-secret

**Parameters:**

Name | Type |
------ | ------ |
`path` | string |

**Returns:** *`Promise<IVaultResponse<void>>`*

___

###  listSecrets

▸ **listSecrets**(`path`: string): *`Promise<IVaultResponse<IListSecretsResponse>>`*

*Defined in [secrets-engines/Kv1SecretEngine.ts:53](https://github.com/theogravity/vault-tacular/blob/68ec17c/src/secrets-engines/Kv1SecretEngine.ts#L53)*

returns a list of key names at the specified location. Folders are suffixed with /. The input
must be a folder; list on a file will not return a value. Note that no policy-based filtering
is performed on keys; do not encode sensitive information in key names. The values themselves
are not accessible via this command.

**`link`** https://www.vaultproject.io/api/secret/kv/kv-v1.html#list-secrets

**Parameters:**

Name | Type |
------ | ------ |
`path` | string |

**Returns:** *`Promise<IVaultResponse<IListSecretsResponse>>`*

___

###  readSecret

▸ **readSecret**(`path`: string): *`Promise<IVaultResponse<IReadSecretResponse>>`*

*Defined in [secrets-engines/Kv1SecretEngine.ts:28](https://github.com/theogravity/vault-tacular/blob/68ec17c/src/secrets-engines/Kv1SecretEngine.ts#L28)*

This endpoint retrieves the secret at the specified location

**`link`** https://www.vaultproject.io/api/secret/kv/kv-v1.html#read-secret

**Parameters:**

Name | Type |
------ | ------ |
`path` | string |

**Returns:** *`Promise<IVaultResponse<IReadSecretResponse>>`*