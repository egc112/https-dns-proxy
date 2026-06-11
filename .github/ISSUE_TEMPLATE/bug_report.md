---
name: Bug report
about: Report a bug in the https-dns-proxy service
title: "[https-dns-proxy] "
labels: bug
assignees: stangri

---

**Before opening this issue**

If you're using the LuCI web UI, please decide first whether the bug is in the UI or the service:

- The setting saves correctly but `https-dns-proxy` still misbehaves → file here.
- Service-level commands (e.g. `service https-dns-proxy status`) reproduce the bug without the UI → file here.
- Only the UI looks broken / a control does nothing / Save & Apply produces a JS error → file at [stangri/luci-app-https-dns-proxy](https://github.com/stangri/luci-app-https-dns-proxy/issues) instead.

**Describe the bug**

A clear and concise description of what the bug is.

**To reproduce**

1.
2.

**Expected behavior**

A clear and concise description of what you expected to happen.

**Diagnostic info**

Please run the following and paste the output (you can mask sensitive parts). See [Getting Help](https://docs.mossdef.org/https-dns-proxy/#getting-help) in the docs for context.

```sh
ubus call system board
curl -V
dnsmasq --version
https-dns-proxy -V
uci export dhcp
uci export network
uci export https-dns-proxy
service https-dns-proxy status
service https-dns-proxy info
nslookup google.com 127.0.0.1:5053
```
