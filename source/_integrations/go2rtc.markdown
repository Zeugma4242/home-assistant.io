---
title: go2rtc
description: Instructions on how to setup go2rtc in Home Assistant.
ha_config_flow: false
ha_release: 2024.11
ha_iot_class: Local Polling
ha_codeowners:
  - '@home-assistant/core'
ha_domain: go2rtc
related:
  - docs: /installation/
---

The go2rtc {% term integration %} will connect to a go2rtc instance and will provide a WebRTC proxy for all your cameras.

If you are using the [`default_config`](/integrations/default_config/) and Home Assistant runs as

- {% term "Home Assistant Operating System" %}
- {% term "Home Assistant Supervised" %}
- {% term "Home Assistant Container" %}
    
the go2rtc integration will be set up automatically and you don't need to do anything.


## Configuration

This integration is part of the [`default_config`](/integrations/default_config/).

The following YAML options are available:

{% configuration %}
debug_ui:
  required: false
  description: Enables the UI of the go2rtc, which helps debugging WebRTC issues. The `debug_ui` should only enabled during debugging as it will expose port 1984 without any authentication!
  default: false
  type: boolean
url:
  required: false
  description: The URL to the selfhosted [go2rtc](https://github.com/AlexxIT/go2rtc/) server
  type: string
{% endconfiguration %}

More information about the go2rtc project can be found on GitHub: https://github.com/AlexxIT/go2rtc/


### Examples

Use a selfhosted instance:

```yaml
go2rtc:
  url: http://my-go2rtc-instance:1984
```

