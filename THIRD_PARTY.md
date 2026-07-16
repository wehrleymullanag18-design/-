# 第三方依赖与授权说明

当前原型未包含下载的第三方飞机、图片、字体或 HDRI 文件。飞机与壁板均由 Three.js 几何体程序化生成，因此不存在外部模型授权风险；外形仅为“A320 级窄体客机近似场景”，不应宣称为制造商官方数字模型。

运行时依赖（已存放于 `vendor/`，不会在访问页面时请求第三方 CDN）：

- Three.js 0.160.0 — MIT License — `https://github.com/mrdoob/three.js`
- Tween.js 23.1.2 — MIT License — `https://github.com/tweenjs/tween.js`
- Draco decoder（可选 GLB 压缩模型）— Apache License 2.0 — `https://github.com/google/draco`

固定版本文件来源为上述项目的官方 npm/Three.js 发布包。版本升级时应同步更新本文件并重新执行浏览器兼容性测试。

完整许可证文本位于 `vendor/licenses/`。

正式接入第三方 GLB、HDRI、纹理、字体或品牌标识时，请在此文件补充：来源 URL、作者、许可证、修改说明、商用权限和署名要求。不得直接抓取航空公司或飞机制造商官网素材用于商业发布。
