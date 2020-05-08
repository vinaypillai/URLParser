# URL Parser
URLParser is a library that helps separate urls into individual components, such as hostname, domain, public suffix domain, tld, and path.

## Installation
### Node.js
``` bash
npm install --save jsurlparser
```

## API
### `URLParser.parse(url)`
Parses url and returns object with following properties.
* `path`: The path following the hostname, if available
* `tld`: The root zone of the url
* `domain`: The second level domain + `tld`
* `hostname`: All subdomains + `domain`
* `publicSuffixDomain`: First private part of url + public suffix.

### `URLParser.hostname(url)`
Parses hostname from url. Returns null if no hostname is found.

### `URLParser.path(url)`
Parses path from url. Returns null if no path is found.

### `URLParser.domain(url)`
Parses path from url. Returns null if no path is found.

### `URLParser.publicSuffixDomain(url)`
Parses public suffix domain and suffix from url. Defaults to domain if no public suffix is found. Returns null if no domain is found.

### `URLParser.tld(url)`
Parses root zone from url. Returns null if no tld is found.

## Acknowledgements
* Mozilla Foundation's [Public Suffix List](https://publicsuffix.org/)

## License

ISC License (ISC)

Copyright 2020 Vinay Pillai

Permission to use, copy, modify, and/or distribute this software for any purpose with or without fee is hereby granted, provided that the above copyright notice and this permission notice appear in all copies.

THE SOFTWARE IS PROVIDED "AS IS" AND THE AUTHOR DISCLAIMS ALL WARRANTIES WITH REGARD TO THIS SOFTWARE INCLUDING ALL IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS. IN NO EVENT SHALL THE AUTHOR BE LIABLE FOR ANY SPECIAL, DIRECT, INDIRECT, OR CONSEQUENTIAL DAMAGES OR ANY DAMAGES WHATSOEVER RESULTING FROM LOSS OF USE, DATA OR PROFITS, WHETHER IN AN ACTION OF CONTRACT, NEGLIGENCE OR OTHER TORTIOUS ACTION, ARISING OUT OF OR IN CONNECTION WITH THE USE OR PERFORMANCE OF THIS SOFTWARE.
THE SOFTWARE.