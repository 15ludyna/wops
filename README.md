# Wops 
A simple package to work with password in JS / TS

## Installation
npm
```
npm install wops 
```
yarn
```
yarn add wops
```

## Usage
```typescript
import { 
  generatePassword, 
  validatePassword, 
  hashPassword,
  checkPasswordStrength
} from 'wops'

const password = generatePassword(10, true)

const { hash, salt } = hashPassword("YOUR PASSWORD")

const isValid = validatePassword("YOUR PASSWORD", salt, hash)

const passwordStrength = checkPasswordStrength("YOUR PASSWORD")
```

## Functions

<dl>
<dt><a href="#generatePassword">generatePassword(length, useUpper, useNumber, useSpecial)</a> ⇒ <code>string</code></dt>
<dd><p>Generates a password according to the specified parameters</p>
</dd>
<dt><a href="#hashPassword">hashPassword(pswd)</a> ⇒ <code><a href="#HashAndSalt">HashAndSalt</a></code></dt>
<dd><p>Given a Password, hash it with a salt, then return the hash and the salt</p>
</dd>
<dt><a href="#validatePassword">validatePassword(inpPswd, salt, storedHash)</a> ⇒ <code>boolean</code></dt>
<dd><p>Given an input password a salt and an hash
Does the given password match with the hash?</p>
</dd>
<dt><a href="#checkPasswordStrength">checkPasswordStrength(pswd)</a></dt>
<dd><p>The checkPasswordStrength function checks how strong the entered password is</p>
</dd>
</dl>

## Typedefs

<dl>
<dt><a href="#HashAndSalt">HashAndSalt</a> : <code>Object</code></dt>
<dd></dd>
</dl>

<a name="generatePassword"></a>

## generatePassword(length, useUpper, useNumber, useSpecial) ⇒ <code>string</code>
Generates a password according to the specified parameters

**Kind**: global function
**Returns**: <code>string</code> - password

| Param | Type |
| --- | --- |
| length | <code>string</code> |
| useUpper | <code>boolean</code> |
| useNumber | <code>boolean</code> |
| useSpecial | <code>boolean</code> |

<a name="hashPassword"></a>

## hashPassword(pswd) ⇒ [<code>HashAndSalt</code>](#HashAndSalt)
Given a Password, hash it with a salt, then return the hash and the salt

**Kind**: global function
**Returns**: [<code>HashAndSalt</code>](#HashAndSalt) - object containing the hash and the salt used

| Param | Type |
| --- | --- |
| pswd | <code>string</code> |

<a name="validatePassword"></a>

## validatePassword(inpPswd, salt, storedHash) ⇒ <code>boolean</code>
Does the given password match with the hash?

**Kind**: global function
**Returns**: <code>boolean</code> - does hash(inpPswd + salt) === storedHash?

| Param | Type |
| --- | --- |
| inpPswd | <code>string</code> |
| salt | <code>string</code> |
| storedHash | <code>string</code> |

<a name="checkPasswordStrength"></a>

## checkPasswordStrength(pswd)
The checkPasswordStrength function checks how strong the entered password is

**Kind**: global function

| Param | Type |
| --- | --- |
| pswd | <code>string</code> |

<a name="HashAndSalt"></a>

## HashAndSalt : <code>Object</code>
**Kind**: global typedef
**Properties**

| Name | Type | Description |
| --- | --- | --- |
| hash | <code>string</code> | The hash we got |
| salt | <code>string</code> | The salt used for hashing |
