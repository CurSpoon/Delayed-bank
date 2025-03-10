
# 时间管理债务计算器 🕒💰

一个基于浏览器的工具，帮助用户量化和管理因拖延产生的“时间债务”，通过可视化统计和激励机制提升时间管理效率。


## 主要功能

### ⏱️ 债务计算
- **延迟记录**：输入0-1440分钟的延迟时间，自动计算债务
- **分期机制**：超过3小时的延迟自动分3期偿还
- **每日利息**：未偿还债务每日产生0.15%利息

### 🎯 激励机制
- **连续奖励**：连续3天无延迟可减免20%债务
- **成就统计**：实时显示未拖延天数、当前天数等数据

### 💰 还款管理
- 支持灵活还款操作
- 自动记录还款历史
- 可视化分期还款计划

## 使用说明

### 快速开始
1. 克隆本仓库：
```bash
git clone https://github.com/CurSpoon/Delayed-Bank.git
```
3. 用浏览器打开 `index.html`

### 基本操作
1. **记录延迟**：
   - 输入延迟时间（分钟）
   - 点击「添加记录」
   
2. **偿还债务**：
   - 输入还款金额
   - 点击「还债」

3. **每日更新**：
   - 每天结束时点击「新的一天」
   - 自动计算利息和到期分期

### 数据持久化
- 使用浏览器本地存储自动保存进度
- 清除缓存会重置数据

## 技术细节

### 技术栈
- **前端**：HTML5 / CSS3 / JavaScript
- **存储**：LocalStorage
- **样式**：CSS自定义属性 + 响应式设计

### 核心算法
```javascript
// 债务计算示例
function calculateEstimatedDebt(delayTime) {
    if (delayTime > 0 && delayTime < 180) {
        return delayTime * 2;
    } else if (delayTime >= 180) {
        return delayTime * 2; 
    }
    return 0;
}

// 每日利息计算
totalDebt = formatNumber(totalDebt * 1.0015);
```

## 贡献指南
欢迎通过 Issue 或 PR 参与改进：
1. Fork 本仓库
2. 创建特性分支 (`git checkout -b feature/新功能`)
3. 提交修改 (`git commit -m '添加新功能'`)
4. 推送分支 (`git push origin feature/新功能`)
5. 发起 Pull Request

## 许可证
[MIT License](LICENSE)


