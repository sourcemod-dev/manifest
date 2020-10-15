# SP Manifest

A repository of include manifest files

## Overview

The manifests directory contains a collection of TOML files or descriptors

An example TOML descriptor file

```toml
[meta]
name = "TTT"
description = "Trouble in terroist town"
author = "Bara"

[source]
type = "git"
merge = true
repository = "https://github.com/TroubleInTerroristTown/Public.git"
patterns = [
    "addons/sourcemod/scripting/include/ttt.inc",
    "addons/sourcemod/scripting/include/ttt_*.inc"
]
```

All the manifest files are processed by the documentation generator via cron (every Sunday) or file trigger.

Manifest files are processed and converted to bundle files in the `bundles` branch that will be consumed by the CDN
