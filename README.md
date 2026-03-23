# 黄金价格走势图可视化

一个功能完整的黄金价格可视化工具，支持K线图和多指标分析。

## 功能特性

- 📊 **K线图（蜡烛图）**
  - 支持6小时、1天、3天、7天四种时间框架切换
  - 鼠标悬停显示详细价格信息（开盘价、最高价、最低价、收盘价）
  - 红色表示上涨，绿色表示下跌（符合中国市场习惯）

- 📈 **分析指标折线图**
  - MA5：5日移动平均线
  - MA10：10日移动平均线
  - MA20：20日移动平均线
  - RSI：相对强弱指标
  - 所有指标均可通过按钮控制显示/隐藏

- 🎨 **界面设计**
  - 响应式设计，支持移动端
  - 现代化渐变色UI
  - 实时价格显示

## 技术栈

- HTML5
- CSS3 (Flexbox布局，渐变色设计)
- JavaScript (ES6+)
- Chart.js (图表库)

## 本地运行

直接在浏览器中打开 `index.html` 文件即可。

## GitHub Pages 部署

### 方法一：通过GitHub网页界面（推荐）

1. 访问你的仓库：https://github.com/TANG-YIN/Au
2. 点击仓库顶部的 **Settings** 标签
3. 在左侧菜单中找到 **Pages** 选项
4. 在 **Source** 部分，选择 **Deploy from a branch**
5. 分支选择 **main**，文件夹选择 **/ (root)**
6. 点击 **Save** 保存
7. 等待1-2分钟，页面顶部会显示部署完成
8. 部署完成后，你的网站将可以通过以下URL访问：
   ```
   https://tang-yin.github.io/Au/
   ```

### 方法二：使用GitHub CLI（如果已安装）

```bash
# 启用GitHub Pages
gh api repos/TANG-YIN/Au/pages -X POST -f source[branch]=main -f source[path]=/
```

### 方法三：使用GitHub API

```bash
# 需要先设置GitHub Token
export GITHUB_TOKEN="your_personal_access_token"

# 启用GitHub Pages
curl -X POST \
  -H "Authorization: token $GITHUB_TOKEN" \
  -H "Accept: application/vnd.github.v3+json" \
  https://api.github.com/repos/TANG-YIN/Au/pages \
  -d '{"source":{"branch":"main","path":"/"}}'
```

## 查看部署状态

启用GitHub Pages后，你可以：
- 访问 https://github.com/TANG-YIN/Au/settings/pages 查看部署状态
- 部署完成后，URL会显示在页面顶部
- 通常需要1-3分钟完成部署

## 自定义说明

- 当前使用的是模拟数据，如需连接真实API，请修改JavaScript中的 `generateGoldData` 函数
- 所有数据和计算逻辑都在前端完成，无需后端服务器
- 可以根据需要修改颜色方案和布局

## 许可证

MIT License
