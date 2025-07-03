# AIEC 职场素养培训平台

一个专为新员工设计的在线学习平台，提供AI智能测验和学习进度跟踪功能。

## 🌟 平台特色

### 核心功能
- **📚 结构化学习内容** - 7个核心章节，系统化职场素养培训
- **🎧 音频学习** - 每章配备专业音频讲解
- **📊 学习进度跟踪** - 实时记录学习进展和完成状态
- **🤖 AI智能测验** - 基于章节内容的个性化测试系统
- **👨‍💼 管理后台** - 学员数据统计和学习分析
- **🌙 深色模式** - 护眼的深色主题切换
- **🌍 多语言支持** - 中文版和阿拉伯语版

### 技术架构
- **前端**: HTML5 + CSS3 + JavaScript + TailwindCSS
- **数据存储**: LocalStorage (免费方案)
- **AI功能**: 基于规则的智能问答系统
- **部署**: 静态文件，支持GitHub Pages/Vercel免费托管

## 🚀 快速开始

### 1. 本地运行
```bash
# 克隆项目
git clone https://github.com/sunke550/zhichangsuyang-final.git

# 进入项目目录
cd zhichangsuyang-final

# 直接打开 login.html 开始使用
open login.html
```

### 2. 在线访问
访问已部署的版本：[https://sunke550.github.io/zhichangsuyang-final/login.html](https://sunke550.github.io/zhichangsuyang-final/login.html)

## 👥 用户角色

### 新员工 (Employee)
- **登录账户**: `employee` / `123456`
- **主要功能**:
  - 按章节学习课程内容
  - 收听音频讲解
  - 查看个人学习进度
  - 参加AI智能测验
  - 标记章节完成状态

### 管理员 (Admin)
- **登录账户**: `admin` / `admin123`
- **主要功能**:
  - 查看所有学员学习数据
  - 统计学习完成情况
  - 分析测验成绩分布
  - 监控学员活跃度

## 📖 学习内容

### 7个核心章节
1. **🗺️ 战略进化蓝图** - 从AI教练到战略引擎
2. **🎯 新人职场素养** - 掌握"凡事有回应"四个层次
3. **⚙️ 第一工作原则** - 机制优于意愿
4. **🏛️ 成长四大支柱** - 四轮驱动的成长生态系统
5. **📈 团队成长模型** - 价值交换与环境策略
6. **🔬 产品学科化建设** - 拥抱AI增量思维
7. **💖 组织心法** - 在变化中保持稳定

### 学习路径
```
登录 → 选择章节 → 阅读内容 → 收听音频 → 标记完成 → 参加测验
```

## 🧠 AI智能测验系统

### 测验特点
- **📝 多题型支持**: 单选题、多选题、问答题
- **🎯 个性化评估**: 基于关键词匹配的智能评分
- **📊 即时反馈**: 实时显示答题结果和建议
- **🏆 成绩记录**: 自动保存测验历史和最高分

### 评分标准
- **90-100分**: 🌟 优秀！完全掌握
- **80-89分**: 👍 良好！稍加复习可达优秀
- **70-79分**: 📚 及格！建议重新学习
- **< 70分**: 💪 需努力！请回到学习页面

## 📊 管理后台功能

### 数据统计
- **用户概览**: 总用户数、完成学习用户数
- **学习分析**: 平均学习进度、章节完成率
- **测验统计**: 平均分数、测验参与度
- **活跃度**: 用户最后活动时间

### 可视化图表
- **📈 学习进度分布图** - 展示不同进度段的用户分布
- **📊 章节完成度** - 各章节的整体完成情况

## 🛠️ 部署指南

### 方案一：GitHub Pages (免费)
1. Fork此项目到您的GitHub账户
2. 在仓库设置中开启GitHub Pages
3. 选择source为main分支
4. 访问：`https://yourusername.github.io/zhichangsuyang-final/login.html`

### 方案二：Vercel (免费)
1. 在 [Vercel](https://vercel.com) 注册账户
2. 连接GitHub仓库
3. 一键部署
4. 获得自定义域名

### 方案三：本地服务器
```bash
# 使用Python简易服务器
python -m http.server 8000

# 或使用Node.js
npx http-server

# 访问 http://localhost:8000/login.html
```

## 💾 数据存储

### LocalStorage结构
```javascript
// 用户登录信息
userRole: "employee" | "admin"
username: "用户名"
loginTime: "登录时间"

// 学习进度 (按用户存储)
progress_username: {
  "章节ID": {
    visited: true,
    completed: false,
    visitTime: "访问时间",
    completionTime: "完成时间"
  }
}

// 测验结果 (按用户存储)
quiz_results_username: {
  "章节ID": {
    score: 85,
    maxScore: 100,
    percentage: 85,
    timestamp: "测验时间"
  }
}
```

## 🔧 自定义配置

### 添加新章节
1. 修改 `index.html` 中的章节数据
2. 在 `audio/` 目录添加对应音频文件
3. 更新 `quiz.html` 中的题目数据库

### 修改测验题目
编辑 `quiz.html` 中的 `questionBank` 对象：
```javascript
const questionBank = {
  "章节ID": [
    {
      question: "题目内容",
      type: "essay|single|multiple",
      points: 10,
      keywords: ["关键词1", "关键词2"] // 用于问答题评分
    }
  ]
}
```

### 样式自定义
- 主题颜色：修改 TailwindCSS 的 indigo 色系
- 字体：更改 `font-family: 'Inter'`
- 布局：调整 grid 和 flex 布局

## 📱 移动端适配

平台采用响应式设计，完美支持：
- 📱 手机 (320px+)
- 📱 平板 (768px+)
- 💻 桌面 (1024px+)

## 🔒 安全考虑

- 前端验证：基本的用户角色检查
- 数据隔离：用户数据按用户名分别存储
- 建议增强：生产环境建议添加后端验证

## 🎯 未来功能规划

- [ ] 真实的用户注册系统
- [ ] 集成真实AI API (OpenAI/ChatGPT)
- [ ] 数据库后端 (Node.js + MongoDB)
- [ ] 学习路径推荐算法
- [ ] 社交学习功能 (讨论区)
- [ ] 学习证书生成
- [ ] 邮件通知系统

## 🤝 贡献指南

1. Fork 项目
2. 创建特性分支 (`git checkout -b feature/AmazingFeature`)
3. 提交更改 (`git commit -m 'Add some AmazingFeature'`)
4. 推送到分支 (`git push origin feature/AmazingFeature`)
5. 创建 Pull Request

## 📄 许可证

本项目采用 MIT 许可证 - 查看 [LICENSE](LICENSE) 文件了解详情

## 📞 联系支持

如有问题或建议，请：
- 📧 发送邮件至: [support@aiec.example.com](mailto:support@aiec.example.com)
- 🐛 在GitHub上提交issue
- 💬 加入我们的讨论群

---

**祝您学习愉快！🎉** 