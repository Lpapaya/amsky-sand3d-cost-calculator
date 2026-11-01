# AMSKY 砂型3D打印运行成本与投资测算器 V4.0

网站：https://lpapaya.github.io/amsky-sand3d-cost-calculator/

独立项目，包含可调产能、用砂配比、回用次数、固化剂、配套投资、运行成本和四页可视化PDF方案。默认值为可编辑初步预算，应以实际报价、工艺试验及账单校准。数据仅保存在本机浏览器。联系：amsky3d@gmail.com。

index.html为图片、样式和脚本全部内嵌的独立网页。GitHub Pages使用main分支根目录。完整可维护源码以Base64文本备份保存在amsky-calculator-v4-source.zip.b64。下载原始文件后先解码为ZIP：

```sh
python3 -c 'import base64,pathlib; pathlib.Path("source.zip").write_bytes(base64.b64decode(pathlib.Path("amsky-calculator-v4-source.zip.b64").read_bytes()))'
```

解压source.zip后运行npm ci、npm test、npm run typecheck、npm run build；将dist/calculator-offline.html重命名为index.html上传根目录即可更新。src/main.tsx引用App.tsx和domain.ts，旧components/utils为历史参考。

回用上限1–8次，默认8，不含新砂首次使用；首次回用在存放≤3天且砂斗≤7天窗口内免补，第三次总使用起默认补2‰、可调1–3‰。超窗按全部需补的保守预算计算，实际须工艺确认。到限退出与补新砂影响成本，不简单按砂量除以次数。再生线综合砂费默认200元/吨成型基砂，其他成本另计。轮廓剔除及有效回收率按实测校准；本工具不替代正式报价、技术协议或质量验证。
