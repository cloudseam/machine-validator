
# Machine Spec Validator

This project contains the machine specifications and a validator to validate a given JSON structure against the spec.

## Usage

```bash
npm install @cloudseam/machine-validator
yarn add @cloudseam/machine-validator
```

In your code, require the project, which is simply the validating function.

```js
const validator = require('@cloudseam/machine-validator');
const machineConfig = {}; // Load this from a file or somewhere else

validator(machineConfig)
    .then(() => console.log("Success"))
    .catch((err) => console.error("Failure", err);)
```

## API

`validator(machineConfig)`

**machineConfig** - object of the machine config, possibly loaded from a YAML file

**return** - the machine config if valid. Otherwise, throws an error describing the fault.

**NOTE:** The validator makes heavy use of the [Joi](https://github.com/hapijs/joi) project because is makes validating JSON structures easy. However, some of the error messages are fairly cryptic. That will be fixed up in future releases.

## Development

Simply run `docker-compose up -d` to spin up a local dev environment.

