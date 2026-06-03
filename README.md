# Mobile Proxy Rules

Public generated rule files for mobile proxy clients.

These files are generated from the private OpenClash source rule file. This
repository does not contain proxy nodes, subscription links, passwords, tokens,
or full client profiles.

## Files

- `shadowrocket_rules.list` - rules for Shadowrocket.
- `v2rayng_routing_rules.json` - routing rule array for v2rayNG custom routing.
- `v2rayng_routing.json` - complete routing object wrapper for Xray/V2Ray-style
  configs.

## Raw URLs

Shadowrocket:

```text
https://raw.githubusercontent.com/birdy0000/openclash-mobile-rules/main/shadowrocket_rules.list
```

v2rayNG routing rules:

```text
https://raw.githubusercontent.com/birdy0000/openclash-mobile-rules/main/v2rayng_routing_rules.json
```

v2rayNG routing object:

```text
https://raw.githubusercontent.com/birdy0000/openclash-mobile-rules/main/v2rayng_routing.json
```

## Policy Mapping

- `DIRECT` becomes direct connection.
- `REJECT*` becomes reject/block.
- OpenClash proxy groups such as `USA` and `GLOBAL` become the default proxy.
