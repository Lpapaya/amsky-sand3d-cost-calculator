# AMSKY 砂型3D打印成本与投资测算器 V5.0

- [打开 V5.0](https://lpapaya.github.io/amsky-sand3d-cost-calculator/)
- [打开 V4.1](https://lpapaya.github.io/amsky-sand3d-cost-calculator/versions/v4.1/)
- [V4.1 稳定版本及回退说明](https://github.com/Lpapaya/amsky-sand3d-cost-calculator/releases/tag/v4.1-stable)

配套投资默认仅计入初始投入，可选择同时计入折旧。外协比较显示运行持平产量和目标回本产量。年度效益可分别与外协打印或传统造型比较，按本厂数据估算年净效益、回收期和 5 年累计 ROI。

网页在浏览器本机计算与保存方案。V5.0 首次读取 V4.1 方案并复制到独立保存空间。下载 index.html 可离线打开。

## 源码与构建

下载 amsky-calculator-v5-source.zip.b64 后，在本机解码并解压。

```sh
python3 -c "import base64,pathlib; pathlib.Path('amsky-calculator-v5-source.zip').write_bytes(base64.b64decode(pathlib.Path('amsky-calculator-v5-source.zip.b64').read_bytes()))"
unzip amsky-calculator-v5-source.zip -d amsky-calculator-v5-source
cd amsky-calculator-v5-source
npm ci
npm test
npm run typecheck
npm run build
```

构建生成 dist/index.html 与 dist/calculator-offline.html。GitHub Pages 首页使用自包含版本。回退时将 v4.1-stable 的发布文件通过新提交恢复到 main，核实 Pages 发布成功。
