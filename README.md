# Winston API Documentation
The Winston API documentation is your resource for integrating Winston in to your next application!

With in this repository you will find resource on how to integrate Winston directly in to your life.

Winston is driving to create a place where you can learn to earn. We are building tools including a web3 shopping cart, social media integrations and other application integrations that allow you to utilze the Winston network and build on our decentralized financial future.

1. [General API Documentation](./README.md)
1. [Members API Documentation](./README.md)
1. [Card Services API Documentation](./README.md)
1. [Merchant Services API Documentation](./README.md)

# Authentication Headers
  In order to use some of Winston's API features you will need to authenticate with your API Developers Account Credentials. You can get your API Access by creating an account [here](./README.md)
 
```
{
  'address': 'String',
  'token': 'String',
  'hash': 'String',
}
```

_Developer Note_ [Todo](./note-access-headers.md)


## Forming an API Signature

Object returned from [/authenticate](./Authentication.md)
```JavaScript
const message = {
  address,// String
  token,  // String
  hash,   // String
}
```

## Creating the Signature

```Javascript
const signer = ethers.Wallet.getSigner();
const headerSignature = signer.signMessage(JSON.stringfy(message));
```

## Setting X-Headers

 API requests will require the following x-headers:

```
{
  'x-api-user': `{address}`,
  'x-session-token': `{accessToken}`,
  'x-session-signature': `{headerSignature}`,
}
```

Need help, reach out to us in [Discord](https://discord.gg/rickletoken)
or send us an [Email](mailto:admin@winston.services)
