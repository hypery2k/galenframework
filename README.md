# Galenframework commandline helpers

[Galen](http://galenframework.com) allows automated testing of look and feel for your responsive websites.

[![Build Status](https://travis-ci.org/hypery2k/galenframework-cli.svg?branch=master)](https://travis-ci.org/hypery2k/galenframework-cli)
[![Build status](https://ci.appveyor.com/api/projects/status/fbwy88pc9ia6429w/branch/master?svg=true)](https://ci.appveyor.com/project/hypery2k/galenframework-cli/branch/master)
[![License](https://img.shields.io/github/license/mashape/apistatus.svg)](LICENSE)
[![Code Climate](https://codeclimate.com/github/hypery2k/galenframework-cli/badges/gpa.svg)](https://codeclimate.com/github/hypery2k/galenframework-cli)
[![Coverage Status](https://coveralls.io/repos/github/hypery2k/galenframework-cli/badge.svg?branch=master)](https://coveralls.io/github/hypery2k/galenframework-cli?branch=master)

The [core](core/) module is just the node wrapper (NodeJS 8+) for [Galen](http://galenframework.com) and can be used within CI environments

[![Known Vulnerabilities](https://snyk.io/test/github/hypery2k/galenframework-cli/badge.svg?targetFile=core%2Fpackage.json)](https://snyk.io/test/github/hypery2k/galenframework-cli?targetFile=core%2Fpackage.json)

The [cli](cli/) module is a command line module (NodeJS 8+) for [Galen](http://galenframework.com). This includes the core above and webdriver downloads for different browsers. You can also use the [docker image](https://hub.docker.com/r/galenframework/cli/) for easier setup.

[![Known Vulnerabilities](https://snyk.io/test/github/hypery2k/galenframework-cli/badge.svg?targetFile=cli%2Fpackage.json)](https://snyk.io/test/github/hypery2k/galenframework-cli?targetFile=cli%2Fpackage.json) [![Docker Build Status](https://img.shields.io/docker/build/galenframework/cli.svg)](https://hub.docker.com/r/galenframework/cli/)

## Donation

Feel free to [donate via Paypal](https://www.paypal.com/cgi-bin/webscr?cmd=_s-xclick&hosted_button_id=H8TR8246RCDJG) or [Bitcoins ](bitcoin:3NKtxw1SRYgess5ev4Ri54GekoAgkR213D): bitcoin:3NKtxw1SRYgess5ev4Ri54GekoAgkR213D

[![Bitcoin](https://martinreinhardt-online.de/assets/img/bitcoin.png)](bitcoin:3NKtxw1SRYgess5ev4Ri54GekoAgkR213D)
 Also via [greenaddress](https://greenaddress.it/pay/GA3ZPfh7As3Gc2oP6pQ1njxMij88u/)

## Docker

### Usage


```
docker run -v $(pwd)/galenframework-cli/core/test/:/var/test_scripts galenframework/cli galen test /var/test_scripts/...
```

### Troubleshooting

npm install throws "cannot access parent directories: Permission denied":
```
npm config set user 0
npm config set unsafe-perm true
```
