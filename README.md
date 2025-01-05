# ASN-China

实时更新的中国ASN和IP数据库。

## 特征

- 每日自动更新
- 可靠且准确的来源

## 在代理应用中使用

mihomo(clash.meta)

```
rule-providers:
  reject:
    type: http
    behavior: classical
    url: "https://raw.githubusercontent.com/Lycofuture/ASN-China/main/ASN.China.yaml"
    path: ./ruleset/ChinaASN.yaml
    interval: 86400
```

Surge

```
[Rule]
# > China ASN List
RULE-SET, https://raw.githubusercontent.com/Lycofuture/ASN-China/main/ASN.China.list, Direct
```

Quantumult X

```
[filter_remote]
# China ASN List
https://raw.githubusercontent.com/Lycofuture/ASN-China/main/ASN.China.list, tag=ChinaASN, force-policy=direct, update-interval=86400, opt-parser=true, enabled=true
```
