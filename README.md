# steampunk-sfdx-plugin

Utilities developed by Steampunk (@SteampunkFoundry)

[![Version](https://img.shields.io/npm/v/chipp-sfdx-plugins.svg)](https://npmjs.org/package/steampunk-sfdx-plugin)
[![Codecov](https://codecov.io/gh/ctchipps/chipp-sfdx-plugins/branch/master/graph/badge.svg)](https://codecov.io/gh/ctchipps/steampunk-sfdx-plugin)
[![Known Vulnerabilities](https://snyk.io/test/github/ctchipps/chipp-sfdx-plugins/badge.svg)](https://snyk.io/test/github/steampunk-sfdx-plugin)
[![Downloads/week](https://img.shields.io/npm/dw/chipp-sfdx-plugins.svg)](https://npmjs.org/package/steampunk-sfdx-plugin)
[![License](https://img.shields.io/npm/l/chipp-sfdx-plugins.svg)](https://github.com/SteampunkFoundry/steampunk-sfdx-plugin/blob/master/package.json)

<!-- toc -->
* [Contents](#contents)
* [Setup](#setup)
* [Commands](#commands)
<!-- tocstop -->
<!-- install -->

## Setup

### **Install as a SalesforceDX Plugin**

```bash  
sfdx plugins:install steampunk-sfdx-plugin
```

You will be prompted to confirm that you want to install an unsigned plugin. Choose "yes"

```bash
This plugin is not digitally signed and its authenticity cannot be verified. Continue installation y/n?: y
```

To whitelist this plugin, [add an entry for it in $HOME/.config/sfdx/unsignedPluginWhiteList.json](https://developer.salesforce.com/blogs/2017/10/salesforce-dx-cli-plugin-update.html).

### **Install from source**

1. Clone the repository

```bash  
git clone https://github.com/SteampunkFoundry/steampunk-sfdx-plugin.git
```

1. Link the plugin:

```bash
sfdx plugins:link .
```
