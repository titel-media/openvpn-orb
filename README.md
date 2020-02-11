# openvpn-orb [![CircleCI Build Status](https://circleci.com/gh/titel-media/openvpn-orb.svg?style=shield "CircleCI Build Status")](https://circleci.com/gh/titel-media/openvpn-orb) [![CircleCI Orb Version](https://img.shields.io/badge/endpoint.svg?url=https://badges.circleci.io/orb/titel-media/wireguard)][reg-page] [![GitHub License](https://img.shields.io/badge/license-MIT-lightgrey.svg)](https://raw.githubusercontent.com/titel-media/openvpn-orb/master/LICENSE)

> CircleCI orb for connecting to a OpenVPN

It allows you to establish a OpenVPN connection from within a CircleCI build job.


## Prerequisites

The following environment variables need to be set in CircleCI either directly or via a context:

- OPENVPN_CONFIG

Variable has to contain a Base64 encoded OpenVPN config file

```shell
$ cat <<EOF | base64
> [Interface]
> PrivateKey = <private-key>=
> Address = 192.0.0.1/32
> DNS = 10.0.0.13
>
> [Peer]
> PublicKey = <public-key>=
> AllowedIPs = 0.0.0.0/0
> Endpoint = 50.210.50.3:51820
> EOF
```

If `AllowedIPs` is "0.0.0.0/0" the CircleCI container will stop responding and the build will crush. To avoid this "0.0.0.0/0" will be replaced with the public IP of the current job while execution.

See [CircleCI Documentation](https://circleci.com/docs/2.0/env-vars) for instructions on how you would set this up.


## Usage

Example use as well as a list of available executors, commands, and jobs are available on this orb's [registry page][reg-page].


## Resources

[CircleCI Orb Registry Page][reg-page] - The official registry page for this orb will all versions, executors, commands, and jobs described.
[CircleCI Orb Docs](https://circleci.com/docs/2.0/orb-intro/#section=configuration) - Docs for using and creating CircleCI Orbs.


## Contributing
We welcome [issues](https://github.com/titel-media/openvpn-orb/issues) to and [pull requests](https://github.com/titel-media/openvpn-orb/pulls) against this repository!

### Publishing

New versions of this orb are published by pushing a SemVer git tag by the Community & Partner Engineering Team.

[reg-page]: https://circleci.com/orbs/registry/orb/titel-media/wireguard
