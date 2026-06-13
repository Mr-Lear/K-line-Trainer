# A股 K线训练器

> 一个基于 GitHub Pages 的 A 股 5 分钟 K 线数据查看工具，随机抽取近三年某一天的交易数据并可视化展示。

## 功能

- **股票代码查询**：输入 6 位 A 股代码（如 `600036`），查看最新完整交易日的 5 分钟 K 线
- **随机日期回测**：自动从近三年中随机选取一个交易日，展示该日分时 K 线走势
- **K 线图展示**：蜡烛图 + 成交量柱，支持拖拽缩放、悬浮查看详情
- **关键数据卡片**：开盘/收盘/最高/最低/涨跌幅/成交额一目了然

## 数据源

数据来自 **[东方财富](https://push2his.eastmoney.com/)** 公开 HTTP API，与 baostock 数据同源。

> ⚠️ 数据仅供学习参考，不构成投资建议。

## 使用方式

### 在线访问

打开 [https://gmo99.github.io/K-line-Trainer/](https://gmo99.github.io/K-line-Trainer/)

### 本地运行

```bash
# 克隆仓库
git clone https://github.com/gmo99/K-line-Trainer.git

# 直接用浏览器打开 index.html
# 或使用任意 HTTP 服务器 (例如 Python)
python -m http.server 8000
# 访问 http://localhost:8000
```

## 技术栈

- 纯前端静态页面 (HTML + CSS + JavaScript)
- [ECharts](https://echarts.apache.org/) 
- 东方财富开放 API — 实时股票数据
- 适配桌面端和移动端

## 部署到 GitHub Pages

1. 在仓库 `Settings → Pages` 中：
   - **Source**: `Deploy from a branch`
   - **Branch**: `main`，目录 `/ (root)`
2. 保存后等待几分钟，页面即可通过 `https://<用户名>.github.io/K-line-Trainer/` 访问

## 本地开发

```bash
# 安装依赖（可选，用于本地 HTTP 服务）
npm install -g http-server   # 或使用 python -m http.server
http-server . -p 8080
```

## License

MIT
