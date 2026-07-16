# METAPANEL AERO 网站原型

这是一个可直接部署到任意静态托管平台的沉浸式 3D 产品网站，无需构建步骤。

## 目录

- `index.html`：完整页面、Three.js 场景、滚动镜头、交互与响应式逻辑
- `data/performance.json`：独立演示数据接口
- `THIRD_PARTY.md`：第三方依赖与素材授权说明
- `DEPLOY.md`：公开发布说明

## 数据替换

保持 `data/performance.json` 的字段结构不变即可替换为真实试验数据。正式发布前必须把 `dataStatus` 改为 `VERIFIED`，并补充试验编号、日期、工况、测点和不确定度说明。

## 真实飞机模型替换

在 `index.html` 的模块脚本之前设置：

```html
<script>
window.METAPANEL_CONFIG = {
  aircraftModelUrl: "./assets/aircraft.glb"
};
</script>
```

模型建议以机头朝 `-Z`、机尾朝 `+Z`，单位统一为米。当前程序化 A320 级近似模型会在 GLB 成功加载后自动隐藏；加载失败则自动回退。

## 运行要求

网站使用 ES Modules，公开部署后可直接运行。离线场景需把 Three.js、Tween.js 和 Draco 解码器下载到本地并修改 import map。

## 浏览器与性能

- 桌面目标：60 FPS
- 低核心数、低内存或小屏设备自动降低像素比并关闭阴影
- 遵循 `prefers-reduced-motion`
- 外部 GLB 加载失败时保留程序化模型

