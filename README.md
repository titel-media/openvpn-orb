# openvpn-orb [![CircleCI Build Status](https://circleci.com/gh/titel-media/openvpn-orb.svg?style=shield "CircleCI Build Status")](https://circleci.com/gh/titel-media/openvpn-orb) [![CircleCI Orb Version](https://img.shields.io/badge/endpoint.svg?url=https://badges.circleci.io/orb/titel-media/openvpn)][reg-page] [![GitHub License](https://img.shields.io/badge/license-MIT-lightgrey.svg)](https://raw.githubusercontent.com/titel-media/openvpn-orb/master/LICENSE)

> CircleCI orb for connecting to OpenVPN

It allows you to establish a OpenVPN connection from within a CircleCI build job.


## Prerequisites

The following environment variables need to be set in CircleCI either directly or via a context:

- VPN_CONFIG

Variable has to contain a Base64 encoded OpenVPN config file


See [CircleCI Documentation](https://circleci.com/docs/2.0/env-vars) for instructions on how you would set this up.


## Usage

Example use as well as a list of available executors, commands, and jobs are available on this orb's [registry page][reg-page].


## Resources

* [CircleCI Orb Registry Page][reg-page] - The official registry page for this orb will all versions, executors, commands, and jobs described.
* [CircleCI Orb Docs](https://circleci.com/docs/2.0/orb-intro/#section=configuration) - Docs for using and creating CircleCI Orbs.


## Contributing
We welcome [issues](https://github.com/titel-media/openvpn-orb/issues) to and [pull requests](https://github.com/titel-media/openvpn-orb/pulls) against this repository!

### Publishing

New versions of this orb are published by creating a new [release][] with a [SemVer][] tag by the Community & Partner Engineering Team.
Afterwards the actual publishing is being executed by the [CI](./.circleci/config.yml)

[reg-page]: https://circleci.com/orbs/registry/orb/titel-media/openvpn
[release]: https://github.com/titel-media/openvpn-orb/releases/new
[SemVer]: https://semver.org
