> **[Vault client for node.js](../README.md)**

[Globals](../globals.md) / [ITokenAuth](../modules/itokenauth.md) / [ICreateTokenPayload](itokenauth.icreatetokenpayload.md) /

# Interface: ICreateTokenPayload

## Hierarchy

* **ICreateTokenPayload**

## Index

### Properties

* [display_name](itokenauth.icreatetokenpayload.md#optional-display_name)
* [explicit_max_ttl](itokenauth.icreatetokenpayload.md#optional-explicit_max_ttl)
* [id](itokenauth.icreatetokenpayload.md#optional-id)
* [meta](itokenauth.icreatetokenpayload.md#optional-meta)
* [no_default_policy](itokenauth.icreatetokenpayload.md#optional-no_default_policy)
* [no_parent](itokenauth.icreatetokenpayload.md#optional-no_parent)
* [num_uses](itokenauth.icreatetokenpayload.md#optional-num_uses)
* [period](itokenauth.icreatetokenpayload.md#optional-period)
* [policies](itokenauth.icreatetokenpayload.md#optional-policies)
* [renewable](itokenauth.icreatetokenpayload.md#optional-renewable)
* [ttl](itokenauth.icreatetokenpayload.md#optional-ttl)

## Properties

### `Optional` display_name

• **display_name**? : *string*

*Defined in [interfaces/auth-methods/ITokenAuth.ts:70](https://github.com/theogravity/vault-tacular/blob/68ec17c/src/interfaces/auth-methods/ITokenAuth.ts#L70)*

The display name of the token.

**`default`** "token"

___

### `Optional` explicit_max_ttl

• **explicit_max_ttl**? : *string*

*Defined in [interfaces/auth-methods/ITokenAuth.ts:64](https://github.com/theogravity/vault-tacular/blob/68ec17c/src/interfaces/auth-methods/ITokenAuth.ts#L64)*

If set, the token will have an explicit max TTL set upon it. This maximum token TTL
cannot be changed later, and unlike with normal tokens, updates to the system/mount
max TTL value will have no effect at renewal time -- the token will never be able to
be renewed or used past the value set at issue time.

___

### `Optional` id

• **id**? : *string*

*Defined in [interfaces/auth-methods/ITokenAuth.ts:15](https://github.com/theogravity/vault-tacular/blob/68ec17c/src/interfaces/auth-methods/ITokenAuth.ts#L15)*

The ID of the client token. Can only be specified by a root token. Otherwise,
the token ID is a randomly generated value.

___

### `Optional` meta

• **meta**? : *object*

*Defined in [interfaces/auth-methods/ITokenAuth.ts:27](https://github.com/theogravity/vault-tacular/blob/68ec17c/src/interfaces/auth-methods/ITokenAuth.ts#L27)*

A map of string to string valued metadata. This is passed through to the audit devices.

#### Type declaration:

● \[▪ **key**: *string*\]: string

___

### `Optional` no_default_policy

• **no_default_policy**? : *boolean*

*Defined in [interfaces/auth-methods/ITokenAuth.ts:40](https://github.com/theogravity/vault-tacular/blob/68ec17c/src/interfaces/auth-methods/ITokenAuth.ts#L40)*

If true the default policy will not be contained in this token's policy set.

___

### `Optional` no_parent

• **no_parent**? : *boolean*

*Defined in [interfaces/auth-methods/ITokenAuth.ts:35](https://github.com/theogravity/vault-tacular/blob/68ec17c/src/interfaces/auth-methods/ITokenAuth.ts#L35)*

If true and set by a root caller, the token will not have the parent token of the caller.
This creates a token with no parent.

___

### `Optional` num_uses

• **num_uses**? : *number*

*Defined in [interfaces/auth-methods/ITokenAuth.ts:77](https://github.com/theogravity/vault-tacular/blob/68ec17c/src/interfaces/auth-methods/ITokenAuth.ts#L77)*

The maximum uses for the given token.
This can be used to create a one-time-token or limited use token.
The value of 0 has no limit to the number of uses.

___

### `Optional` period

• **period**? : *string*

*Defined in [interfaces/auth-methods/ITokenAuth.ts:84](https://github.com/theogravity/vault-tacular/blob/68ec17c/src/interfaces/auth-methods/ITokenAuth.ts#L84)*

If specified, the token will be periodic; it will have no maximum TTL
(unless an "explicit-max-ttl" is also set) but every renewal will use the given period.
Requires a root/sudo token to use.

___

### `Optional` policies

• **policies**? : *`Array<string>`*

*Defined in [interfaces/auth-methods/ITokenAuth.ts:22](https://github.com/theogravity/vault-tacular/blob/68ec17c/src/interfaces/auth-methods/ITokenAuth.ts#L22)*

A list of policies for the token. This must be a subset of the policies belonging to the
token making the request, unless root. If not specified, defaults to all the policies
of the calling token.

___

### `Optional` renewable

• **renewable**? : *boolean*

*Defined in [interfaces/auth-methods/ITokenAuth.ts:49](https://github.com/theogravity/vault-tacular/blob/68ec17c/src/interfaces/auth-methods/ITokenAuth.ts#L49)*

Set to false to disable the ability of the token to be renewed past its initial TTL.
Setting the value to true will allow the token to be renewable up to the system/mount
maximum TTL.

**`default`** true

___

### `Optional` ttl

• **ttl**? : *string*

*Defined in [interfaces/auth-methods/ITokenAuth.ts:56](https://github.com/theogravity/vault-tacular/blob/68ec17c/src/interfaces/auth-methods/ITokenAuth.ts#L56)*

The TTL period of the token, provided as "1h", where hour is the largest suffix.
If not provided, the token is valid for the default lease TTL,
or indefinitely if the root policy is used.