

<div align="center">  
  <h1>nostr-ld</h1>
</div>

<div align="center">  
<i>nostr-ld</i>
</div>

---

<div align="center">
<h4>Documentation</h4>
</div>

---

[![GitHub license](https://img.shields.io/badge/license-MIT-blue.svg)](https://github.com/nostrapps/nostr-ld/blob/gh-pages/LICENSE)
[![npm](https://img.shields.io/npm/v/nostr-ld)](https://npmjs.com/package/nostr-ld)
[![npm](https://img.shields.io/npm/dw/nostr-ld.svg)](https://npmjs.com/package/nostr-ld)
[![Github Stars](https://img.shields.io/github/stars/nostrapps/nostr-ld.svg)](https://github.com/nostrapps/nostr-ld/)

# Nostr-LD

Nostr-LD is a powerful and extensible library for transforming Nostr events and profiles into JSON-LD format. By leveraging JSON-LD, a W3C standard, Nostr-LD allows Nostr data to be interpreted and used by a wide range of tools and applications, enhancing interoperability and integration across the web.

## Table of Contents

- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Contributing](#contributing)
- [License](#license)

## Features

- **Event-LD**: Transforms Nostr events into JSON-LD format.
- **Profile-LD**: Transforms Nostr profiles into JSON-LD format.
- Easy extensibility to support additional Nostr types in the future.
- Promotes decentralization and domain independence.

## Installation

```bash
npm install nostr-ld
```

## Usage

### Event-LD

```javascript
import { eventld } from 'nostr-ld';

const event = '{...}'; // Your Nostr event here.
const jsonLD = eventld(event);

console.log(JSON.stringify(jsonLD, null, 2));
```

### Profile-LD

```javascript
import { profileld } from 'nostr-ld';

const user = '...'; // Your user pubkey here.
const mergedData = '{...}'; // Merged user data.
const jsonLD = profileld(user, mergedData);

console.log(JSON.stringify(jsonLD, null, 2));
```

## Why Nostr-LD?

The adoption of JSON-LD for Nostr events and profiles brings several benefits:

- **Interoperability**: JSON-LD is a W3C standard widely adopted, which enables data from Nostr to be easily consumed by a broad range of tools and applications.
- **Decentralization**: By storing data in a decentralized manner, in the `/.well-known/nostr/` directory, Nostr-LD helps to maintain the decentralized nature of Nostr and doesn't put pressure on individual relays.
- **Semantic Web**: JSON-LD is a key technology in the Semantic Web, enabling Nostr data to be part of the larger web of data.

## Contributing

We welcome contributions! Please see our [contributing guide](CONTRIBUTING.md) for more details.

## License

[MIT](LICENSE.md)

---

By embracing standards like JSON-LD, Nostr-LD aims to keep Nostr open, interoperable, and ready for the future of the web. We hope you find this library useful in your Nostr-related projects.

## License

- MIT
