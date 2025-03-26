<!-- markdownlint-disable MD033 -->
<h1 align="center">
<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/sighupio/distribution/refs/heads/main/docs/assets/white-logo.png">
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/sighupio/distribution/refs/heads/main/docs/assets/black-logo.png">
  <img alt="Shows a black logo in light color mode and a white one in dark color mode." src="https://raw.githubusercontent.com/sighupio/distribution/refs/heads/main/docs/assets/white-logo.png">
</picture><br/>
  vSphere Add-On Module
</h1>
<!-- markdownlint-enable MD033 -->

![Release](https://img.shields.io/badge/Latest%20Release-v1.4.0-blue)
![License](https://img.shields.io/github/license/sighupio/fury-kubernetes-vsphere?label=License)
![Slack](https://img.shields.io/badge/slack-@kubernetes/fury-yellow.svg?logo=slack&label=Slack)

<!-- <SD-DOCS> -->

**vSphere Add-On Module** is an add-on module for the [SIGHUP Distribution (SD)][kfd-repo] that provides
packages to integrate vSphere with Kubernetes.

If you are new to SD please refer to the [official documentation][sd-docs] on how to get started with SD.

## Overview

**vSphere Add-On Module** uses a collection of open source tools to install Kubernetes in an vSphere environment.

## Packages

The following packages are included in the vSphere Add-On Module module:

| Package                                        | Version  | Description                                                                   |
| ---------------------------------------------- | -------- | ----------------------------------------------------------------------------- |
| [vsphere-cm](katalog/vsphere-cm)               | `1.30.0` | Kubernetes Cloud Provider for vSphere                                         |
| [vsphere-csi](katalog/vsphere-csi)             | `3.3.1`  | vSphere storage Container Storage Interface (CSI) plugin                      |

Click on each package to see its full documentation.

## Compatibility

Check the [compatibility matrix][compatibility-matrix] for additional information about the compatibility of the module.

## Usage

### Prerequisites

| Tool                    | Version   | Description                                                                                                                                                |
| ----------------------- | --------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [furyctl][furyctl-repo] | `>=0.29.0` | The recommended tool to download and manage SD modules and their packages. To learn more about `furyctl` read the [official documentation][furyctl-repo]. |

### Download the packages

List the bases in a `Furyfile.yml` file

```yaml
bases:
  - name: vsphere
    version: v1.4.0
```

> See `furyctl` [documentation][furyctl-repo] for additional details about `Furyfile.yml` format.

1. Execute `furyctl legacy vendor -H` to download the katalog

2. Inspect the downloaded katalog inside `./vendor/katalog/vsphere`

3. Check each package documentation for the configuration with vSphere

<!-- Links -->

[furyctl-repo]: https://github.com/sighupio/furyctl
[compatibility-matrix]: https://github.com/sighupio/fury-kubernetes-vsphere/blob/master/docs/COMPATIBILITY_MATRIX.md
[kfd-repo]: https://github.com/sighupio/distribution
[sd-docs]: https://docs.kubernetesfury.com/docs/distribution/

<!-- </SD-DOCS> -->

<!-- <FOOTER> -->

### Reporting Issues

In case you experience any problems with the module, please [open a new issue](https://github.com/sighupio/fury-kubernetes-vsphere/issues/new/choose).

## License

This module is open-source and it's released under the following [LICENSE](LICENSE).

<!-- </FOOTER> -->
