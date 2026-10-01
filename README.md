# surge-rules

自用 Surge 规则集、模块与配置。

## 目录

- `rule/ai.list` — AI 规则集（基于 blankmagic，去掉了 Apple Intelligence 分区）
- `rule/apple-direct.list` — 9 个苹果服务域名，直连兜底（App Store CDN、iCloud 专用代理、Siri 后端、地图/定位/Spotlight）
- `rule/` 下其他 `.list` — 上游规则集的镜像（ACL4SSR、blackmatrix7），与上游内容一致
- `modules/BlockHTTPDNS.sgmodule` — 拦截国产 App 自建 HTTPDNS，强制回退系统 DNS
- `modules/SkipChinaMobile.sgmodule` — 中国移动 App / 139 邮箱 / 咪咕跳过代理检测
- `sub_optimized.conf` — 主配置（**脱敏版**：已移除 MITM CA 私钥与 MTProto secret，拉取后需在本地重新填入 CA 信息）

## 调用地址（jsDelivr）

```
https://cdn.jsdelivr.net/gh/dadad897949/surge-rules@main/rule/ai.list
https://cdn.jsdelivr.net/gh/dadad897949/surge-rules@main/rule/apple-direct.list
```
