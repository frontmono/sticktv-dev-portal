---
title: JSON API Basic Format
position: 1
---

**URL**:
https://{*server domain*}/{*version*}/{*service name*}

All API request must contain SSID in Cookie or GET parameter.
SSID can get from serviceLogin API

**Result**

JSON Dictionary (in root level)

|Name|Note|
|---|---|
|code|if success "000", otherwise error code [more info](/sub-json-api/error.html).|
|msg|description of code(only in error)|
|detail|detail of error message|
|data|N/A|
