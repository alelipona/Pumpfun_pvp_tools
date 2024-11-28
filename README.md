# Pump 交易助手

- 一个基于Electron的Pumpfun Pvp 交易工具，支持代币创建、买入、卖出、拉盘等功能。
- 免费接口无需pumpportal高额手续费 http://154.201.73.182:3456/api/trade-local
 ## 图示
<img width="1280" alt="image" src="https://github.com/user-attachments/assets/00efb7f1-72a1-449d-800f-fb3ada5386bc">
<img width="1280" alt="image" src="https://github.com/user-attachments/assets/e6b21f84-90d2-45f1-a24b-7af983b957fd">
 
 ## 项目结构
```
Pumpfun_pvp_tools/
├── src/
│   ├── create.js      # 代币创建相关功能
│   ├── sell.js        # 代币卖出相关功能
│   ├── lapan.js       # 拉盘相关功能
│   ├── monitor.js     # 交易监控功能
│   ├── tradem.js      # 交易管理功能
│   ├── wallet.js      # 钱包管理功能
│   ├── electron.js    # Electron主进程
│   └── index.html     # 主界面
├── .env               # 环境变量配置
├── .env.example       # 环境变量示例
├── package.json       # 项目配置文件
└── README.md          # 项目说明文档
```
### 主要模块说明
- **create.js**: 实现代币创建和初始买入功能
- **sell.js**: 实现代币批量卖出功能
- **lapan.js**: 实现自动拉盘策略
- **monitor.js**: 实现实时交易监控
- **tradem.js**: 处理交易相关的核心逻辑
- **wallet.js**: 实现钱包管理、资金分发和归集
- **electron.js**: Electron应用的主进程
- **index.html**: 应用界面的HTML实现

## 主要功能
### 1. 代币交易
- 创建并买入代币
- 一键卖出代币
- 自动拉盘功能
- 实时交易监控

### 2. 钱包管理
- 支持多钱包管理(创建钱包1-5和拉盘钱包1-100)
- 一键生成钱包
- SOL批量分发
- SOL批量归集

### 3. 实时监控
- 实时显示交易信息
- 显示买入/卖出数据
- 支持自动监控新代币
- 交易进度实时展示

## 安装说明

1. 克隆项目 
2. 安装依赖
3. 配置.env文件
4. 运行项目

```bash
# 克隆项目
git clone https://github.com/vnxfsc/Pumpfun_pvp_tools
# 进入项目目录
cd Pumpfun_pvp_tools

# 安装依赖
npm install

# 运行项目
 npm start
```
## 环境配置
在项目根目录创建 `.env` 文件，配置以下必要参数：
```env
# RPC节点配置
HELIUS_RPC_URL=你的Helius RPC URL
# 主钱包配置（用于创建代币）
WALLET_PRIVATE_KEY_1=主钱包私钥
# 买入钱包配置（钱包2-5自动生成）
WALLET_PRIVATE_KEY_1_AMOUNT=0
WALLET_PRIVATE_KEY_2_AMOUNT=3.00
WALLET_PRIVATE_KEY_3_AMOUNT=3.50
WALLET_PRIVATE_KEY_4_AMOUNT=3.30
WALLET_PRIVATE_KEY_5_AMOUNT=3.00
# 拉盘钱包配置（钱包1-100自动生成）
WALLET_LAPAN_KEY_1=
...
WALLET_LAPAN_KEY_100=
``` 
## 使用指南 
### 1. 钱包准备
 - 在钱包管理页面，使用"一键生成"功能生成买入钱包(2-5)和拉盘钱包(1-100)
 - 使用"分发"功能向各个钱包分发适量SOL
 
 ### 2. 创建代币
 - 在创建配置页面设置各个买入钱包的买入金额
 - 返回主页，点击"创建并买入"按钮
 - 等待交易完成，系统会自动记录代币地址
 
 ### 3. 拉盘操作
 - 在主页设置拉盘参数：
   * 延迟时间：2-3秒（可调）
   * 每次使用钱包数：1-3个（可调）
   * 每笔交易金额：0.1-0.3 SOL（可调）
 - 点击"拉盘"按钮开始自动拉盘
 - 可随时点击按钮停止拉盘 
 ### 4. 卖出操作
 - 确认代币地址已正确显示
 - 点击"卖出"按钮
 - 系统将自动从所有钱包卖出代币
 
 ### 5. 资金回收
 - 交易结束后，使用钱包管理页面的"归集"功能
 - 将所有钱包的SOL归集到主钱包
 
 ## 注意事项 
 1. 安全建议
    - 妥善保管主钱包私钥
    - 定期备份生成的钱包私钥
    - 不要将私钥泄露给他人
 
 2. 操作建议
    - 确保主钱包有足够的SOL
    - 分发SOL时预留足够的gas费
    - 使用前测试小额交易
    - 定期检查钱包余额 
 3. 网络相关
    - 使用可靠的RPC节点
    - 保持网络稳定
    - 避免频繁大额交易 
 ## 技术支持 
 - 如遇问题请提交Issue
 - 欢迎提交Pull Request改进代码
 - 交流群：[https://t.me/chainbuff](https://t.me/chainbuff) 
 ## 打赏
 - Solana地址：8nMFEMb1MXE8BjTBuAYMuy1mYtwwKNQcm937Y9yy9eHu
 ## 免责声明
  本工具仅供学习研究使用，使用本工具产生的任何后果由使用者自行承担。 
 ## 许可证
  MIT License
