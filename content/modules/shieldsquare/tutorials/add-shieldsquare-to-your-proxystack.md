---
title: Add  Shieldsquare to your proxystack
description: Adding Shieldsquare to your Section proxy stack.
keywords: content delivery network, CDN, shieldsquare, bot blocking, reverse proxies, proxy, proxy template, WAF
weight: 1
---

## Overview

This tutorial will guide you through the process to adding the Shieldsquare module to your proxy stack with default configuration files. This tutorial assumes you've cloned your application's git repository to your local machine.

### Step 1 - Updating section.config.json

1. Add the following object to your **proxystack** array in your **section.config.json** file located in the root of your repository.

```
{
    "name": "shieldsquare",
    "image": "shieldsquare:1.0.0"
}
```

{{% notice note %}}
You can add this module at any index in your proxystack array. We'd recommend adding this module as the first module.
{{% /notice %}}

### Step 2 - Adding default files

1. Create a `shieldsquare` directory in the root of your repository.
1. Create the following files under the **shieldsquare** directory:
    * shieldsquare.json

### Step 3 - Populate the shieldsquare.json file

The `shieldsquare.json` file will have the following format :

{{< gist section-io-gists b239842d77ac093a43fa2fa4b8d36dd9 >}}

The `key` and `deployment_number` will be provided to you by Section. You can contact us at support@section.io.

### Step 4 - Deploy

Commit your changes and push them to the desired branch you are working on. If you run into any issues please contact support@section.io.