# Pteronode (Beta)

## Overview
**Pterodactyl-JS** is a comprehensive Node.js client designed to simplify and streamline server management tasks by interacting with the Pterodactyl API.

*Please note: This is a beta version. Your feedback is invaluable to us for improving the package.*

## Features
### Client Side
- **Account Handling**: Access and update your details, manage 2FA settings, and modify your account information.
- **API Key Operations**: Create, delete, and retrieve API keys seamlessly.
### Application Side


## Installation
Install Pteronode via npm:
```bash
npm install pteronode
```

## Usage
First, import the module and create an instance of the client:
```js
const { PteronodeClient } = require('pteronode');
const client = new PteronodeClient('your-api-key', 'https://your-base-url.com');
```

## Example: Fetching Servers
```js
async function fetchServers() {
    try {
        const servers = await client.getServers();
        console.log(servers);
    } catch (error) {
        console.error('Error fetching servers:', error);
    }
}

fetchServers();
```

## Example: Accounts Details
```js
async function getAccountDetails() {
    try {
        const account = await client.account();
        const details = await account.getDetails();
        console.log(details);
    } catch (error) {
        console.error('Error fetching account details:', error);
    }
}

getAccountDetails();
```

## Contributing
We welcome contributions! Please submit pull requests or report issues to help make Pteronode better.

## License
This project is licensed under the MIT License - see the LICENSE file for details.