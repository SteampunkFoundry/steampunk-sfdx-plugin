# steampunk-sfdx-plugin

Utilities developed by Steampunk (@SteampunkFoundry)

[![Version](https://img.shields.io/npm/v/@steampunk/steampunk-sfdx-plugin.svg)](https://www.npmjs.com/package/@steampunk/steampunk-sfdx-plugin)
[![Known Vulnerabilities](https://snyk.io/test/github/steampunkfoundry/steampunk-sfdx-plugin/badge.svg)](https://snyk.io/test/github/steampunkfoundry/steampunk-sfdx-plugin)
[![Downloads/week](https://img.shields.io/npm/dw/@steampunk/steampunk-sfdx-plugin.svg)](https://www.npmjs.com/package/@steampunk/steampunk-sfdx-plugin)
[![License](https://img.shields.io/npm/l/@steampunk/steampunk-sfdx-plugin.svg)](https://www.npmjs.com/package/@steampunk/steampunk-sfdx-plugin)

<!-- toc -->
* [steampunk-sfdx-plugin](#steampunk-sfdx-plugin)
<!-- tocstop -->

<!-- install -->
## Setup

### **Install as a SalesforceDX Plugin**

```bash  
sfdx plugins:install @steampunk/steampunk-sfdx-plugin
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

## Commands

<!-- commands -->
* [`sfdx punk:data:files:upload -p <filepath> [-u <string>] [--apiversion <string>] [--json] [--loglevel trace|debug|info|warn|error|fatal|TRACE|DEBUG|INFO|WARN|ERROR|FATAL]`](#sfdx-punkdatafilesupload--p-filepath--u-string---apiversion-string---json---loglevel-tracedebuginfowarnerrorfataltracedebuginfowarnerrorfatal)

## `sfdx punk:data:files:upload -p <filepath> [-u <string>] [--apiversion <string>] [--json] [--loglevel trace|debug|info|warn|error|fatal|TRACE|DEBUG|INFO|WARN|ERROR|FATAL]`

Upload multiple files based on a csv as standalone files or linked to records. The csv must have the following headers: Title, PathOnClient. The csv may have the following headers: FirstPublishLocationId. This utility uses the same setup as [Salesforce Dataloader for files](https://help.salesforce.com/articleView?id=000314772&type=1&mode=1).

```
USAGE
  $ sfdx punk:data:files:upload -p <filepath> [-u <string>] [--apiversion <string>] [--json] [--loglevel 
  trace|debug|info|warn|error|fatal|TRACE|DEBUG|INFO|WARN|ERROR|FATAL]

OPTIONS
  -p, --pathtocsv=pathtocsv                                                         (required) path to csv

  -u, --targetusername=targetusername                                               username or alias for the target
                                                                                    org; overrides default target org

  --apiversion=apiversion                                                           override the api version used for
                                                                                    api requests made by this command

  --json                                                                            format output as json

  --loglevel=(trace|debug|info|warn|error|fatal|TRACE|DEBUG|INFO|WARN|ERROR|FATAL)  [default: warn] logging level for
                                                                                    this command invocation

EXAMPLE
  sfdx chipp:data:files:upload -p ~/FilesToUpload.csv
```

_See code: [src/commands/punk/data/files/upload.ts](https://github.com/SteampunkFoundry/steampunk-sfdx-plugin/steampunk-sfdx-plugin/blob/v0.0.1/src/commands/punk/data/files/upload.ts)_
<!-- commandsstop -->
