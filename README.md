# 付款申请书生成器 · 网页版

个人使用的静态浏览器工具，部署到 GitHub Pages 即可运行。没有服务器、登录或实际付款功能。

支持填写、金额大写、Excel/PDF/PNG 导出、ZIP 多格式导出、草稿、历史重载、30 天重复提示、收款方通讯录、月度与收款方汇总、CSV、JSON 备份恢复及红框图片 OCR。

## 与 Windows 版的差异

- 不再依赖安装 Microsoft Excel。Excel 和 PDF/PNG 的版式根据原模板字段布局重新实现，金额大写由网页计算后写入。
- PDF 是可打印的高清图片型 PDF，不包含可选择的文本。
- 多格式通过一个 ZIP 下载；下载位置与同名文件处理由浏览器决定。
- OCR 使用浏览器 Tesseract.js 中文与英文模型，精度可能与原 RapidOCR 不同，须核对后应用。首次使用联网下载公开模型，图片在本机处理。
- 浏览器与设备之间不自动同步。清除网站数据会删除记录，请定期使用历史页的备份功能。
- Windows 版的历史数据库、账户、默认公司名、识图样例没有放入网站。Excel 原文件包含示例账户，因此没有原样发布。

## 发布

上传 index.html、style.css、app.js 和 vendor/，使用 main 分支根目录发布 GitHub Pages。

本地预览：`python -m http.server 8766 --bind 127.0.0.1`。

## 第三方库

- ExcelJS 4.4.0（MIT）：https://github.com/exceljs/exceljs
- jsPDF 2.5.2（MIT）：https://github.com/parallax/jsPDF
- Tesseract.js 5.1.1（Apache-2.0）：https://github.com/naptha/tesseract.js

发行许可位于 vendor/。OCR 引擎与语言模型首次使用时从公开 CDN 下载；申请字段和图片不发送到该 CDN。

