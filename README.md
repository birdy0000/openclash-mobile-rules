# Mobile Proxy Rules

Public generated rule files for mobile proxy clients.

These files are generated from the private OpenClash source rule file. This
repository does not contain proxy nodes, subscription links, passwords, tokens,
or full client profiles.

## Files

- `shadowrocket_rules.list` - import or reference from Shadowrocket rules.
- `shadowrocket.conf` - complete Shadowrocket config for URL import.
- `v2rayng_routing_rules.json` - routing rules array for v2rayNG custom routing.
- `v2rayng_routing.json` - complete routing object wrapper for Xray/V2Ray-style configs.
- `openclash_custom_rules.list` - OpenClash-only custom rules file.
- `clashbox_rules.yaml` - Clash/Mihomo/OpenClash-compatible rules fragment.

## Raw URLs

Shadowrocket:

```text
https://raw.githubusercontent.com/birdy0000/openclash-mobile-rules/main/shadowrocket.conf
```

Shadowrocket rule list:

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

OpenClash custom rules:

```text
https://raw.githubusercontent.com/birdy0000/openclash-mobile-rules/main/openclash_custom_rules.list
```

Clash Box / Clash / Mihomo rules fragment:

```text
https://raw.githubusercontent.com/birdy0000/openclash-mobile-rules/main/clashbox_rules.yaml
```

## Policy Mapping

- `DIRECT` -> direct connection.
- `REJECT*` -> reject/block.
- `USA` -> USA proxy group, filtered by US/USA/United States/America/美国/🇺🇸 node names.
- `DE` -> DE proxy group, filtered by DE/Germany/Deutschland/德国/🇩🇪 node names.
- Shadowrocket and Clash Box map OpenClash default proxy policies such as `GLOBAL` and `代理` to `PROXY`.
- Shadowrocket adds `FINAL,PROXY` to match OpenClash default proxy behavior.
- Clash Box adds `MATCH,PROXY` to match OpenClash default proxy behavior.
- v2rayNG uses outbound tags `proxy`, `usa`, `de`, `direct`, and `block`, with unmatched TCP/UDP traffic going to `proxy`.
- OpenClash uses `openclash_custom_rules.list`, keeping the router source policy names.
- Clash Box uses `PROXY`, `USA`, `DE`, and `DIRECT`; make sure those groups exist in the active Clash Box profile.

## Conversion Notes

- Shadowrocket skipped 1 unsupported or malformed rule(s).
- v2rayNG skipped 1 unsupported or malformed rule(s).
- The source OpenClash rules remain authoritative. Regenerate these files after editing the source.
