# 🎓 学生成绩管理系统 | Student Score Management System

<p align="center">
  <img src="https://img.shields.io/badge/WeChat-小程序-brightgreen" alt="WeChat Mini Program"/>
  <img src="https://img.shields.io/badge/云开发-腾讯云-blue" alt="Tencent Cloud"/>
  <img src="https://img.shields.io/badge/License-商业授权-orange" alt="Commercial License"/>
  <img src="https://img.shields.io/badge/云函数-70+-purple" alt="Cloud Functions"/>
  <img src="https://img.shields.io/badge/页面-29-green" alt="Pages"/>
</p>

<p align="center">
  <b>功能完整的教育管理微信小程序</b><br/>
  A comprehensive education management WeChat Mini Program<br/>
  专为学校、培训机构、教育公司打造
</p>

---

## 📖 项目简介

「学生成绩管理系统」是一款基于微信云开发的完整教育管理解决方案，支持**教师、家长、管理员**三种角色，提供成绩管理、学生管理、班级管理、作业管理、数据分析等全方位功能。

### ✨ 核心特点

- 🎯 **功能完整** - 70+云函数，29个页面，覆盖教育管理核心场景
- 🔒 **安全合规** - 符合《个人信息保护法》，完整的隐私保护方案
- 📊 **数据分析** - ECharts可视化，智能成绩分析
- 📥 **批量操作** - Excel智能解析导入导出，支持集体化学生数据
- ⚡ **性能优异** - 云开发架构，数据库索引优化
- 📚 **文档齐全** - 12份专业文档，43,000+字

---

## 🎯 核心功能

### 👨‍🏫 教师端

#### 教师仪表盘
- 📊 实时数据统计（班级、学生、成绩）
- 📈 可视化数据分析（ECharts）
- 📌 快捷操作入口

#### 班级管理
- ➕ 创建和管理班级
- 👥 学生分配和转班
- 📊 班级统计分析

#### 学生管理
- 👤 学生档案管理
- 📥 Excel批量导入
- 🔍 智能搜索和筛选
- 📞 家长信息管理

#### 成绩管理
- ✍️ 成绩录入和编辑
- 📥 Excel批量导入

#### 作业管理
- 📝 布置作业
- 📋 批改和评分
- 📊 完成率统计
- ⏰ 截止时间提醒

---

### 👨‍👩‍👧 家长端

- 📊 查看孩子成绩
- 📈 成绩趋势分析
- 📝 作业查询提交
- 👶 支持关联多个孩子

---

### 👑 管理员端

- ✅ 教师申请审核
- 👥 用户权限管理
- 📊 全局数据统计
- 🗑️ 账户注销审核
- 🔄 批量班级升级
- 🏷️ 教师分配管理

---

## 🛠️ 技术架构

### 前端技术
```
框架: 微信小程序原生开发
UI: 自定义组件库
图表: ECharts 微信小程序版
样式: WXSS + 响应式设计
```

### 后端技术
```
云开发: 腾讯云云开发
云函数: Node.js 12（70+个）
云存储: 图片和文件存储
```

### 核心特性
- ☁️ **无需服务器** - 基于云开发，零运维
- 🔐 **权限控制** - 三级权限体系
- 🚀 **性能优化** - 数据库索引、分页加载、缓存机制
- 🛡️ **安全防护** - 输入验证、XSS防护、SQL注入防护

---

## 📊 数据统计

| 指标 | 数量 |
|------|------|
| 代码行数 | 55,000+ |
| 云函数 | 70+ |
| 页面数 | 29 |
| 组件数 | 16 |
| 数据库集合 | 12 |
| 技术文档 | 12份（43,000+字）|

---

## 📂 项目结构

```
wechat-student-score-system/
├── miniprogram/              # 小程序前端
│   ├── pages/               # 29个页面
│   ├── components/          # 16个组件
│   ├── utils/              # 工具函数
│   └── images/             # 图片资源
│
├── cloudfunctions/          # 70+云函数
│   ├── bindUser/           # 用户绑定
│   ├── fetchScore/         # 获取成绩
│   ├── importStudentsToDatabase/  # 批量导入学生
│   ├── importScoreFromExcel/      # 批量导入成绩
│   ├── deleteUserAccount/         # 账户注销
│   ├── manageHomework/            # 作业管理
│   ├── getTeacherDashboard/       # 教师仪表盘
│   ├── getAdminDashboard/         # 管理员仪表盘
│   └── ...                        # 其他60+云函数
│
└── docs/                    # 技术文档（12份）
    ├── PRIVACY_POLICY.md           # 隐私保护指引
    ├── PRIVACY_SETUP_GUIDE.md      # 隐私配置指南
    ├── TEACHER_DASHBOARD_README.md # 教师仪表盘说明
    ├── PARENT_MANAGEMENT_DESIGN.md # 家长管理设计
    ├── USER_DELETION_DATABASE_DESIGN.md  # 用户注销设计
    ├── HOMEWORK_DATABASE_DESIGN.md       # 作业系统设计
    └── ...
```

---

## 📊 数据库设计

### 核心数据集合

| 集合名称 | 用途 | 关键字段 |
|---------|------|---------|
| `user` | 用户表 | openId, role  …… |
| `students` | 学生表 | name, studentId …… |
| `classes` | 班级表 | className, grade …… |
| `scores` | 成绩表 | subjectId, score …… |
| `subjects` | 科目表 | subjectName, fullScore …… |
| `homework` | 作业表 | title, deadline …… |
| `homework_submissions` | 作业提交 | homeworkId …… |
| `parent_students` | 家长学生关联 | parentId, studentId …… |
| `teacher_subjects` | 教师科目关联 | teacherId …… |
| `teacher_applications` | 教师申请 | userId  …… |
| `user_deletion_requests` | 注销申请 | userId, deleteType …… |
| `data_deletion_logs` | 删除日志 | userId, deletedData …… |

---

## 🔐 安全与合规

### 隐私保护（符合《个人信息保护法》）
✅ 完整的隐私保护指引页面  
✅ 微信系统自动弹窗（已配置）  
✅ 用户数据导出功能 （部分已完成） 
✅ 账户注销功能（软/硬删除）  
✅ 48小时冷静期机制  
✅ 删除影响分析  

### 数据安全
✅ HTTPS加密传输  
✅ 敏感信息加密存储  
✅ 严格权限控制（云函数验证）  
✅ XSS/SQL注入防护  
✅ 操作审计日志  

---

## 🚀 快速开始

### 环境要求

- 微信开发者工具（最新版）
- 微信基础库 ≥ 3.10.0
- Node.js ≥ 12.x
- 已认证的微信小程序账号
- 腾讯云账号（开通云开发）

### 部署步骤

```bash
# 1. 配置小程序信息
修改 project.config.json 中的 appid
修改 miniprogram/app.js 中的云开发环境ID

# 2. 创建数据库集合（12个）
在云开发控制台创建所有数据库集合

# 3. 上传云函数
在微信开发者工具中批量上传所有云函数

# 4. 配置隐私协议
按照 PRIVACY_SETUP_GUIDE.md 配置隐私保护指引

# 5. 编译运行
点击编译，使用测试账号登录体验

# 6. 提交审核
上传代码 → 提交审核 → 等待通过
```

**详细部署指南**: 请参考购买后提供的完整部署文档

---

## 🎨 功能演示

### 教师仪表盘（实时数据统计和可视化分析）
<img src="/screenshots/TeacherPortal/TeachersPanel.PNG" alt="教师端首页" width="400">

### 成绩分析（ECharts图表展示成绩趋势）
<img src="/screenshots/ParentPortal/Index01.PNG" alt="成绩分析页" width="400">

### Excel导入（批量导入学生）
<img src="/screenshots/TeacherPortal/StudentsImport.PNG" alt="学生信息导入" width="400">

### 隐私合规（完整的隐私保护方案）
<img src="/screenshots/Common/Privacy.PNG" alt="学生信息导入" width="400">

> 💡 更多截图请查看 [/screenshots](/screenshots)

---

## 📚 文档索引

### 核心文档
- [📖 完整产品介绍](PRODUCT_GUIDE.md) - 详细功能说明和界面展示
- [💰 购买和授权](PURCHASE.md) - 价格、购买流程、技术支持
- [🚀 部署指南](docs/DEPLOYMENT_GUIDE.md) - 完整部署步骤（购买后提供）

### 功能文档
- [教师仪表盘说明](TEACHER_DASHBOARD_README.md)
- [家长管理设计](PARENT_MANAGEMENT_DESIGN.md)
- [作业系统部署](HOMEWORK_MVP_DEPLOYMENT_GUIDE.md)

### 数据库设计
- [用户注销数据库设计](USER_DELETION_DATABASE_DESIGN.md)
- [作业系统数据库设计](HOMEWORK_DATABASE_DESIGN.md)

### 配置指南
- [隐私保护配置指南](PRIVACY_SETUP_GUIDE.md)
- [隐私保护指引模板](PRIVACY_POLICY.md)

---

## 👥 用户角色和权限

| 功能 | 管理员 | 教师 | 家长 |
|------|-------|------|------|
| 用户审核 | ✅ | ❌ | ❌ |
| 班级管理 | ✅ | ✅（自己的）| ❌ |
| 学生管理 | ✅ | ✅（自己的）| ❌ |
| 成绩管理 | ✅ | ✅（自己的）| ❌ |
| 成绩查看 | ✅ | ✅ | ✅（孩子的）|
| 作业管理 | ✅ | ✅（自己的）| ❌ |
| 作业查看 | ✅ | ✅ | ✅（孩子的）|
| 数据导出 | ✅ | ✅ | ✅ |
| 账户注销 | ✅ | ✅ | ✅ |

---

## 💡 为什么选择我们？

### ✅ 功能最完整
- 70+云函数，覆盖教育管理全场景
- 29个页面，UI精美，交互流畅
- 三种角色，权限清晰分明

### ✅ 文档最齐全
- 12份专业文档，共43,000+字
- 手把手部署指南
- 清晰的API文档和数据库设计

### ✅ 合规最到位
- 符合《个人信息保护法》
- 完整的隐私保护方案
- 账户注销、数据导出功能齐全

### ✅ 代码最规范
- 注释清晰，易于理解
- 命名统一，遵循最佳实践
- 安全防护完善
- 性能优化到位

### ✅ 部署最快速
- 基于云开发，无需服务器
- 配置简单，高效部署
- 开箱即用

---

## 💰 商业授权

本项目为**商业授权软件**，提供完整源码和技术支持。

### 版本对比

| 项目 | 个人版 | 商业版 ⭐推荐 | 企业版 |
|------|--------|------------|--------|
| 完整源码 | ✅ | ✅ | ✅ |
| 技术文档 | ✅ | ✅ | ✅ |
| 商业授权 | ✅ | ✅ | ✅ |
| 技术支持 | ❌ | ✅ 1个月 | ✅ 3个月 |
| 免费升级 | ❌ | ✅ 3个月 | ✅ 1年 |
| 部署协助 | ❌ | ❌ | ✅ 远程协助 |
| **价格** | **¥暂无** | **¥暂无** | **¥暂无** |

### 购买咨询

📧 **邮箱**: [569070485@qq.com]  
💬 **微信**: [15987364406]  
🔗 **详细介绍**: [PURCHASE.md](PURCHASE.md)

**立即购买，节省5-9个月开发时间！**

---

## 🎁 购买即享

购买任意版本，免费赠送：

1. **隐私合规方案**
   - 完整隐私协议页面（已配置）
   - 符合《个人信息保护法》
   - 买家只需改联系方式

2. **数据库索引优化方案**、
   - 查询速度提升10倍
   - 已配置好的索引

3. **Excel导入导出功能**
   - 批量导入学生
   - 批量导入成绩
   - 智能数据验证

4. **ECharts可视化方案**
   - 多种图表类型
   - 自适应布局

**总价值超过 ¥……！**

---

## 💼 成本对比

| 项目 | 自己开发 | 购买我们的 |
|------|---------|-----------|
| 开发时间 | 3-6个月 | 0天（立即使用）|
| 人力成本 | ¥50,000-100,000 | ¥暂无 |
| 服务器成本 | ¥500/月起 | ¥0（云开发）|
| 技术文档 | 需要自己写 | ✅ 12份齐全 |
| 隐私合规 | 需要咨询律师 | ✅ 已完成（MVP） |

**投资回报率（ROI）：超过 1000%！**

---

## ❓ 常见问题

<details>
<summary><b>Q: 适合什么场景？</b></summary>

A: 适合以下场景：
- ✅ 中小学校成绩管理
- ✅ 培训机构学员管理
- ✅ 补习班成绩记录
- ✅ 教育科技公司产品
- ✅ 软件开发商二次开发

</details>

<details>
<summary><b>Q: 需要购买服务器吗？</b></summary>

A: 不需要！
- ✅ 基于微信云开发
- ✅ 不用买服务器
- ✅ 不用运维
- ✅ 按量付费（小程序免费额度足够）

</details>

<details>
<summary><b>Q: 云开发费用多少？</b></summary>

A: 非常便宜
- 小型机构（100学生）：免费额度足够
- 中型机构（500学生）：约 ¥50-100/月
- 大型机构（1000学生）：约 ¥200-300/月

</details>

<details>
<summary><b>Q: 可以商用吗？</b></summary>

A: 完全可以！
- ✅ 所有版本都包含商业授权
- ✅ 可用于学校、培训机构
- ✅ 可二次开发后出售
- ✅ 可集成到现有系统

限制：
- ❌ 不能直接转售源码
- ❌ 不能移除版权信息

</details>

<details>
<summary><b>Q: 交付周期多久？</b></summary>

A: 
- 付款后 **24小时内** 交付
- 工作日付款，通常 **2小时内** 交付

</details>

更多问题请查看：[完整FAQ](PURCHASE.md#常见问题)

---

## 🔄 更新日志

### v1.0.0 (2025-01-15)
- ✨ 初始版本发布
- ✅ 完整的三端功能（教师/家长/管理员）
- ✅ 作业管理
- ✅ 隐私保护合规功能
- ✅ 账户注销功能
- ✅ 数据导出功能

---

## 📄 许可证

本项目为**商业授权软件**。

**授权范围：**
- ✅ 可用于商业运营
- ✅ 可修改源代码
- ✅ 可二次开发
- ❌ 不可转售源代码
- ❌ 不可移除版权信息

详细授权协议请参考：[LICENSE](LICENSE) 或 [PURCHASE.md](PURCHASE.md)

---

## 🤝 技术支持

### 购买后支持（根据版本）

- **商业版**: 1个月技术支持
- **企业版**: 3个月技术支持 + 远程部署协助

### 支持内容
✅ 部署指导  
✅ 配置问题解答  
✅ Bug修复建议  
✅ 功能使用答疑  
✅ 数据库设计咨询  

### 联系方式

📧 **邮箱**: [569070485@qq.com]  
💬 **微信**: [15987364406]  
⏰ **工作时间**: 周一至周六 9:00-21:00  

---

## 🌟 Star History

如果这个项目对您有帮助，请给我们一个 Star ⭐

[![Star History Chart](https://api.star-history.com/svg?repos=yourusername/wechat-student-score-system&type=Date)](https://star-history.com/#yourusername/wechat-student-score-system&Date)

---

## 🙏 致谢

感谢微信小程序团队和腾讯云团队提供的优秀平台！

---

<p align="center">
  <b>© 2025 学生成绩管理系统 | v1.0.0</b><br>
  <sub>专业 · 完整 · 合规 · 易用</sub>
</p>

<p align="center">
  <a href="PURCHASE.md">💰 立即购买</a> ·
  <a href="PRODUCT_GUIDE.md">📖 产品介绍</a> ·
  <a href="mailto:your-email@example.com">📧 联系我们</a>
</p>

---

**最后更新：2025年10月**





