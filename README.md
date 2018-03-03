# pass-power

Simple tool for checks required conditions in password and sets scores power


## Install

```sh
npm i pass-power
```


## Usage

```js
const {passScore, passAccept} = require('pass-power');
```


## API


#### passScore(val, minPassLength, analysis)

This method return result of validation compliance with input conditions

**val** - Type `string`

**minPassLength** - Type `number`

Minimal password length

**analysis** - Type `array`

In current moment available more common cases:
* hasUppercase
* hasLowercase
* hasDigits
* hasSpecials

```js
passScore('987654321Qq#', 8, ['hasUppercase', 'hasLowercase', 'hasDigits', 'hasSpecials'])
```


#### passAccept(resultObject)

Gets result of method passScore() and return common state of validation (true/false)

**resultObject** - Type `object`

```js
passAccept(passScore('12345', 5, ['hasDigits']))
```


## License

ISC©
