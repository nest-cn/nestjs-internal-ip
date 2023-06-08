## 概述

During the development process of the original internal-ip, the lower version of node had syntax compatibility problems on mac, so it was rebuilt;

## nestjs-internal-ip

Get your internal IP address

## Install

```
npm install nestjs-internal-ip
```

## Usage

```
import {internalIpV6, internalIpV4} from 'nestjs-internal-ip';

console.log(await internalIpV6());
//=> 'fe80::1'

console.log(await internalIpV4());
//=> '10.0.0.79'
```

## API

The package returns the address of the internet-facing interface, as determined from the default gateway. When the address cannot be determined for any reason, undefined will be returned.

The package relies on operating systems tools. On Linux and Android, the ip command must be available, which depending on distribution might not be installed by default. It is usually provided by the iproute2 package. internalIpV6Sync() and internalIpV4Sync() are not supported in browsers and just return undefined.

### internalIpV6()
Returns the internal IPv6 address asynchronously.

### internalIpV4()
Returns the internal IPv4 address asynchronously.

### internalIpV6Sync()
Returns the internal IPv6 address synchronously.

### internalIpV4Sync()
Returns the internal IPv4 address synchronously.
