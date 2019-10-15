# common-services
A module that provides access to common services.

## Updating this README.md
Run `npm run generateReadme` to parse the code for JSDoc comment blocks and recreate this README.md file.

## Install
Run `npm i @pillarwallet/common-services`

## Examples
Instantiate a badges service: <br />
@param - (loggerPath - optional) Specify the file path to which log records are written<br />
@param - (logToFile - optional - default false). Set true to enable logging to a file and file rotation<br />
@param - (dbModels - optional) Pass the Badge and BadgeAward mongoose objects (need for the backend integration)<br />

```javascript
const { Badge, BadgeAward } = require('@pillarwallet/common-models').platform;
const { buildBadgeService } = require('@pillarwallet/common-services');

const BadgeService = buildBadgeService({
  loggerPath: '',
  logToFile: false,
  dbModels: { Badge, BadgeAward },
});

# API

## Members

<dl>
<dt><a href="#Constructor">Constructor</a> ⇒</dt>
<dd><p>This is the constructor of the BadgeService instance.
It allows to set the Configuration keys:</p>
</dd>
<dt><a href="#onUserRegistered">onUserRegistered</a> ⇒</dt>
<dd><p>Method that awards user with a badge for the registration</p>
</dd>
<dt><a href="#onWalletImported">onWalletImported</a> ⇒</dt>
<dd><p>Method that awards user with a badge for the imported wallet</p>
</dd>
<dt><a href="#onConnectionEstablished">onConnectionEstablished</a> ⇒</dt>
<dd><p>Method that awards user with a badge for the first connection</p>
</dd>
<dt><a href="#onTransactionMade">onTransactionMade</a> ⇒</dt>
<dd><p>Method that awards user with a badge for the first transaction made</p>
</dd>
<dt><a href="#onTransactionReceived">onTransactionReceived</a> ⇒</dt>
<dd><p>Method that awards user with a badge for the first transaction received</p>
</dd>
<dt><a href="#selfAward">selfAward</a> ⇒</dt>
<dd><p>Method to award yourself with a badge</p>
</dd>
</dl>

<a name="Constructor"></a>

## Constructor ⇒
This is the constructor of the BadgeService instance.
It allows to set the Configuration keys:

**Kind**: global variable  
**Returns**: Object<BadgeService>  

| Param | Type | Description |
| --- | --- | --- |
| [loggerPath] | <code>String</code> | Specify the file path to which log records are written |
| [logToFile] | <code>Boolean</code> | Enables logging to a file and file rotation |
| [dbModels] | <code>Object</code> | Pass the Badge and BadgeAward mongoose objects |

<a name="onUserRegistered"></a>

## onUserRegistered ⇒
Method that awards user with a badge for the registration

**Kind**: global variable  
**Returns**: Promise<MongoDBObject>  

| Param | Type | Description |
| --- | --- | --- |
| [walletId] | <code>String</code> | Wallet ID |
| [userId] | <code>String</code> | User ID |

<a name="onWalletImported"></a>

## onWalletImported ⇒
Method that awards user with a badge for the imported wallet

**Kind**: global variable  
**Returns**: Promise<MongoDBObject>  

| Param | Type | Description |
| --- | --- | --- |
| [walletId] | <code>String</code> | Wallet ID |
| [userId] | <code>String</code> | User ID |

<a name="onConnectionEstablished"></a>

## onConnectionEstablished ⇒
Method that awards user with a badge for the first connection

**Kind**: global variable  
**Returns**: Promise<MongoDBObject>  

| Param | Type | Description |
| --- | --- | --- |
| [walletId] | <code>String</code> | Wallet ID |
| [userId] | <code>String</code> | User ID |

<a name="onTransactionMade"></a>

## onTransactionMade ⇒
Method that awards user with a badge for the first transaction made

**Kind**: global variable  
**Returns**: Promise<MongoDBObject>  

| Param | Type | Description |
| --- | --- | --- |
| [walletId] | <code>String</code> | Wallet ID |
| [userId] | <code>String</code> | User ID |

<a name="onTransactionReceived"></a>

## onTransactionReceived ⇒
Method that awards user with a badge for the first transaction received

**Kind**: global variable  
**Returns**: Promise<MongoDBObject>  

| Param | Type | Description |
| --- | --- | --- |
| [walletId] | <code>String</code> | Wallet ID |
| [userId] | <code>String</code> | User ID |

<a name="selfAward"></a>

## selfAward ⇒
Method to award yourself with a badge

**Kind**: global variable  
**Returns**: Promise<MongoDBObject>  

| Param | Type | Description |
| --- | --- | --- |
| [badgeType] | <code>String</code> | Badge name |
| [walletId] | <code>String</code> | Wallet ID |
| [userId] | <code>String</code> | User ID |


