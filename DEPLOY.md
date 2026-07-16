# 公开部署

本项目是纯静态站点，部署目录即 `metapanel-aero/`。

## GitHub Pages

将目录内容放到仓库默认分支根目录，或使用 Pages 工作流发布。项目站点位于子路径时，当前相对数据地址无需修改。

## Vercel / Netlify / Cloudflare Pages

- Framework preset：Other / Static
- Build command：留空
- Output directory：`.`
- Root directory：`metapanel-aero`（若仓库还包含其他内容）

## 上线前检查

1. 替换 `business@example.com`、品牌名称和联系信息。
2. 替换演示数据并提供试验依据，或保留醒目的“演示数据”标记。
3. 对新增模型、HDRI、纹理和字体完成授权审查。
4. 配置 CSP、缓存、压缩和自定义域名。
5. 使用真实移动设备检查显存占用、首屏时间和触控交互。
