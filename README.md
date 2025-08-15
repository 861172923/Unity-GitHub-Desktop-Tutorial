# Unity工程通过GitHub桌面版上传到仓库的完整教程

> **适用对象**: Unity开发者、Git初学者、团队协作开发
> **难度等级**: 初级到中级
> **预计时间**: 30-45分钟
> **最后更新**: 2025年1月

## 🎥 视频教程

如果您更喜欢通过视频学习，可以观看我们制作的详细视频教程：

<iframe src="//player.bilibili.com/player.html?isOutside=true&aid=115033350672303&bvid=BV1NLbxzgEXE&cid=31720606696&p=1" scrolling="no" border="0" frameborder="no" framespacing="0" allowfullscreen="true" width="100%" height="500"></iframe>

> **💡 学习建议**:
> - 📺 **视频 + 文档结合**：建议先观看视频了解整体流程，再参考文档进行具体操作
> - 🔄 **边看边做**：可以暂停视频，跟着步骤实际操作
> - 📖 **文档补充**：视频中未涉及的细节可以在下方文档中找到
> - ❓ **问题解决**：遇到问题时可以查看文档中的"常见问题解决"部分

## 📋 目录
1. [🚀 准备工作](#-准备工作)
2. [⚙️ Unity工程配置](#️-unity工程配置)
3. [🖥️ GitHub桌面版设置](#️-github桌面版设置)
4. [📤 创建仓库并上传](#-创建仓库并上传)
5. [📚 版本控制最佳实践](#-版本控制最佳实践)
6. [🔧 常见问题解决](#-常见问题解决)
7. [📖 进阶操作指南](#-进阶操作指南)
8. [🎯 总结与检查清单](#-总结与检查清单)

## 🚀 准备工作

### 📋 检查清单
在开始之前，请确保您已完成以下准备工作：

- [ ] Unity Hub 和 Unity Editor 已安装
- [ ] 拥有GitHub账户
- [ ] 下载并安装GitHub Desktop
- [ ] 准备好要上传的Unity工程

### 1. 软件安装详细步骤

#### 1.1 GitHub账户注册
1. **访问GitHub官网**
   - 打开浏览器，访问 [github.com](https://github.com)
   - 点击右上角 **"Sign up"** 按钮

2. **填写注册信息**
   ```
   Username: 选择一个唯一的用户名（建议使用英文和数字）
   Email: 输入您的邮箱地址
   Password: 设置强密码（至少8位，包含字母和数字）
   ```

3. **验证账户**
   - 完成人机验证
   - 检查邮箱并点击验证链接
   - 选择免费计划（Free plan）

#### 1.2 GitHub Desktop安装

##### 选择合适的版本
根据您的语言偏好选择合适的GitHub Desktop版本：

**官方英文版（推荐）**
- 访问 [desktop.github.com](https://desktop.github.com/)
- 功能最新，更新及时
- 官方技术支持

**中文汉化版（适合英文不太好的用户）**
- 访问 [GitHub Desktop 中文版](https://github.com/zetaloop/Desktop)
- 界面完全中文化，操作更直观
- 基于官方版本汉化，功能完整
- 适合初学者和英文不太好的用户

> **💡 建议**: 如果您的英文水平一般，强烈推荐使用中文版，可以大大降低学习门槛，提高操作效率。

##### 下载和安装步骤

1. **下载GitHub Desktop**

   **官方英文版**:
   - 访问 [desktop.github.com](https://desktop.github.com/)
   - 点击 **"Download for Windows"** 或 **"Download for macOS"**

   **中文汉化版**:
   - 访问 [https://github.com/zetaloop/Desktop](https://github.com/zetaloop/Desktop)
   - 点击 **"Releases"** 查看最新版本
   - 下载对应系统的安装包
   - 等待下载完成

2. **安装步骤**
   - **Windows用户**:
     ```
     1. 双击下载的 .exe 文件
     2. 按照安装向导完成安装
     3. 安装完成后会自动启动
     4. 如果是中文版，界面将显示为中文
     ```

   - **macOS用户**:
     ```
     1. 双击下载的 .dmg 文件
     2. 将GitHub Desktop拖拽到Applications文件夹
     3. 从Applications启动程序
     4. 首次启动可能需要在系统偏好设置中允许运行
     ```

3. **版本对比**
   ```
   功能对比：
                    官方版    中文版
   界面语言         英文      中文
   功能完整性       ✅        ✅
   更新频率         最快      稍慢
   技术支持         官方      社区
   学习难度         中等      较低
   推荐用户         有英文基础  初学者
   ```

4. **首次启动配置**
   - 启动GitHub Desktop（界面语言取决于您选择的版本）
   - 选择 **"Sign in to GitHub.com"**（中文版显示为"登录到GitHub.com"）
   - 输入GitHub账户信息
   - 授权GitHub Desktop访问您的账户

##### 中文版特色功能
如果您选择了中文版，将享受以下便利：
```
中文界面优势：
📝 菜单和按钮全部中文显示
📝 错误信息和提示中文化
📝 操作指引更容易理解
📝 降低学习门槛
📝 提高操作效率
📝 减少误操作风险
```

### 2. 系统要求检查

#### 最低系统要求
- **Windows**: Windows 10 或更高版本
- **macOS**: macOS 10.13 或更高版本
- **磁盘空间**: 至少500MB可用空间
- **网络**: 稳定的互联网连接

#### Unity版本兼容性
- **推荐Unity版本**: 2020.3 LTS 或更高
- **支持的版本**: Unity 2018.4 及以上
- **注意**: 不同Unity版本的项目结构可能略有差异

## ⚙️ Unity工程配置

### 1. Unity工程准备

#### 1.1 创建或打开Unity工程
1. **启动Unity Hub**
   - 双击桌面上的Unity Hub图标
   - 或从开始菜单搜索"Unity Hub"

2. **创建新工程（如果需要）**
   ```
   步骤：
   1. 点击 "New project" 按钮
   2. 选择模板（推荐选择"3D"或"2D"）
   3. 设置项目名称（建议使用英文，避免特殊字符）
   4. 选择保存位置（建议在易于访问的文件夹）
   5. 点击 "Create project"
   ```

3. **打开现有工程**
   ```
   步骤：
   1. 点击 "Open" 按钮
   2. 浏览并选择Unity工程文件夹
   3. 点击 "Select Folder"
   ```

4. **验证工程正常运行**
   - 等待Unity编辑器完全加载
   - 检查Console窗口是否有错误信息
   - 尝试播放场景（点击Play按钮）

#### 1.2 工程结构检查
确保您的Unity工程包含以下基本文件夹结构：
```
YourUnityProject/
├── Assets/                 # 游戏资源文件夹
├── Packages/              # 包管理文件夹
├── ProjectSettings/       # 项目设置文件夹
├── UserSettings/          # 用户设置（不需要版本控制）
└── Library/               # Unity缓存（不需要版本控制）
```

### 2. Unity版本控制配置

> **⚠️ 重要提示**: 这是Unity项目版本控制的核心配置，必须正确设置才能确保团队协作和版本管理的正常运行。

#### 2.1 为什么需要这些配置？

**配置的重要性**：
```
❌ 不配置的后果：
- 资源引用经常丢失 (Missing Reference)
- 团队成员间无法正确同步资源
- 场景和预制体合并时出现问题
- 版本控制工具无法正确处理Unity文件
- 项目在不同电脑上表现不一致

✅ 正确配置的好处：
- 保持资源引用的完整性和一致性
- 支持多人协作开发
- 可以进行有意义的文件比较和合并
- 版本控制历史清晰可读
- 项目在任何环境下都能正常工作
```

**适用版本范围**：
- ✅ **Unity 5.0+**: 完全支持
- ✅ **Unity 2018.4 LTS+**: 强烈推荐
- ✅ **Unity 2020.3 LTS+**: 行业标准
- ✅ **Unity 2022.3 LTS+**: 默认最佳实践

#### 2.2 详细配置步骤

##### 步骤1: 打开项目设置
1. **方法一：使用菜单**
   ```
   路径：Edit → Project Settings
   ```

2. **方法二：使用快捷键**
   ```
   Windows: Ctrl + Shift + ,
   Mac: Cmd + ,
   ```

3. **验证设置窗口**
   - 确认Project Settings窗口已打开
   - 左侧应显示设置分类列表

##### 步骤2: 配置版本控制模式
1. **定位设置位置**
   - 在左侧面板选择 **"Editor"**
   - 向下滚动找到 **"Version Control"** 部分

2. **设置Version Control Mode**
   ```
   当前设置: [显示当前值]
   目标设置: Visible Meta Files

   选项说明:
   - Hidden Meta Files: 隐藏.meta文件（不推荐）
   - Visible Meta Files: 显示.meta文件（推荐）
   - Perforce: 专用于Perforce版本控制系统
   ```

3. **为什么选择Visible Meta Files？**
   ```
   .meta文件的作用:
   📁 存储资源的唯一标识符(GUID)
   📁 保存导入设置和配置
   📁 维护资源间的引用关系
   📁 确保跨平台兼容性
   📁 支持版本控制系统追踪
   ```

##### 步骤3: 配置资源序列化模式
1. **定位序列化设置**
   - 在同一个Editor设置页面
   - 找到 **"Asset Serialization"** 部分

2. **设置Asset Serialization Mode**
   ```
   当前设置: [显示当前值]
   目标设置: Force Text

   选项说明:
   - Mixed: 混合格式（部分二进制，部分文本）
   - Force Binary: 强制二进制格式（不推荐）
   - Force Text: 强制文本格式（推荐）
   ```

3. **为什么选择Force Text？**
   ```
   文本格式的优势:
   📝 可以查看和比较文件内容
   📝 支持智能合并和冲突解决
   📝 版本控制工具可以显示有意义的差异
   📝 文件损坏时更容易恢复
   📝 便于代码审查和调试

   二进制格式的问题:
   ❌ 无法进行文本比较
   ❌ 冲突时难以手动解决
   ❌ 版本历史不可读
   ❌ 合并时容易出错
   ```

##### 步骤4: 应用和验证设置
1. **保存设置**
   - 点击窗口底部的 **"Apply"** 按钮
   - 等待Unity处理设置更改
   - 关闭Project Settings窗口

2. **验证配置生效**
   ```
   检查方法:
   1. 重新打开Project Settings → Editor
   2. 确认Version Control Mode显示为"Visible Meta Files"
   3. 确认Asset Serialization Mode显示为"Force Text"
   ```

#### 2.3 配置后的变化

##### 文件系统变化
**配置前**:
```
Assets/
├── Scripts/
│   └── PlayerController.cs
└── Scenes/
    └── MainScene.unity
```

**配置后**:
```
Assets/
├── Scripts/
│   ├── PlayerController.cs
│   └── PlayerController.cs.meta      ← 新增的meta文件
└── Scenes/
    ├── MainScene.unity
    └── MainScene.unity.meta           ← 新增的meta文件
```

##### 文件内容变化
**场景文件示例**:
```yaml
配置前 (二进制): [不可读的二进制数据]

配置后 (文本):
%YAML 1.1
%TAG !u! tag:unity3d.com,2011:
--- !u!29 &1
OcclusionCullingSettings:
  m_ObjectHideFlags: 0
  serializedVersion: 2
  m_OcclusionBakeSettings:
    smallestOccluder: 5
    smallestHole: 0.25
    backfaceThreshold: 100
```

#### 2.4 团队协作影响

##### 多人开发场景对比
**场景1: 未正确配置**
```
开发者A: 创建预制体 → 提交代码
开发者B: 拉取代码 → 预制体引用丢失 → 需要重新设置
结果: 浪费时间，容易出错 ❌
```

**场景2: 正确配置**
```
开发者A: 创建预制体 → .meta文件包含GUID → 提交代码
开发者B: 拉取代码 → 所有引用保持完整 → 直接可用
结果: 无缝协作，高效开发 ✅
```

#### 2.5 常见问题和解决方案

##### 问题1: 设置后项目变慢
**原因**: 文本序列化可能略微影响加载速度
**解决方案**:
- 这是正常现象，影响很小
- 开发阶段的便利性远超性能损失
- 发布版本可以使用构建优化

##### 问题2: .meta文件太多
**原因**: 每个资源都会生成对应的.meta文件
**解决方案**:
- 这是必要的，不要删除.meta文件
- 确保.meta文件也被版本控制追踪
- 在.gitignore中不要忽略.meta文件

##### 问题3: 现有项目如何迁移
**解决方案**:
```
迁移步骤:
1. 备份整个项目
2. 应用新的版本控制设置
3. 重新导入所有资源 (Assets → Reimport All)
4. 检查所有场景和预制体的引用
5. 提交所有更改到版本控制
```

#### 2.3 验证配置
1. **检查.meta文件**
   - 在文件资源管理器中打开Unity工程文件夹
   - 进入Assets文件夹
   - 确认每个资源文件都有对应的.meta文件

2. **检查场景文件**
   - 打开Scenes文件夹
   - 用文本编辑器打开.unity场景文件
   - 确认内容是可读的文本格式（而非二进制）

### 3. 创建.gitignore文件

#### 3.1 什么是.gitignore文件
.gitignore文件告诉Git哪些文件和文件夹不需要进行版本控制。对于Unity工程，这非常重要，因为：
- Unity会生成大量临时文件和缓存
- 这些文件会频繁变化且体积庞大
- 上传这些文件会浪费存储空间和带宽

#### 3.2 创建.gitignore文件步骤

1. **使用文本编辑器创建**
   ```
   步骤：
   1. 打开记事本（Windows）或TextEdit（Mac）
   2. 将下面的内容复制粘贴到编辑器中
   3. 保存文件名为 ".gitignore"（注意前面的点）
   4. 将文件保存到Unity工程的根目录
   ```

2. **Unity专用.gitignore内容**
   ```gitignore
   # ===================================
   # Unity生成的文件和文件夹
   # ===================================
   [Ll]ibrary/
   [Tt]emp/
   [Oo]bj/
   [Bb]uild/
   [Bb]uilds/
   [Ll]ogs/
   [Uu]ser[Ss]ettings/

   # ===================================
   # Unity缓存和临时文件
   # ===================================
   *.tmp
   *.user
   *.userprefs
   *.pidb
   *.booproj
   *.svd
   *.pdb
   *.mdb
   *.opendb
   *.VC.db

   # ===================================
   # Unity特定文件
   # ===================================
   *.unitypackage
   *.app

   # ===================================
   # 操作系统生成的文件
   # ===================================
   # Windows
   Thumbs.db
   ehthumbs.db
   Desktop.ini

   # macOS
   .DS_Store
   .DS_Store?
   ._*
   .Spotlight-V100
   .Trashes

   # ===================================
   # IDE和编辑器文件
   # ===================================
   # Visual Studio
   *.suo
   *.user
   *.userosscache
   *.sln.docstates
   .vs/

   # Visual Studio Code
   .vscode/

   # JetBrains Rider
   .idea/

   # ===================================
   # 其他常见忽略文件
   # ===================================
   # 崩溃报告
   sysinfo.txt

   # Unity Cloud Build
   /[Bb]uild/
   /[Bb]uilds/

   # Autogenerated Jetbrains Rider plugin
   [Aa]ssets/Plugins/Editor/JetBrains*
   ```

#### 3.3 验证.gitignore文件
1. **检查文件位置**
   - 确认.gitignore文件在Unity工程根目录
   - 与Assets、ProjectSettings文件夹在同一级别

2. **检查文件内容**
   - 用文本编辑器打开.gitignore文件
   - 确认内容正确无误
   - 注意文件编码应为UTF-8

#### 3.4 常见问题解决
- **Windows无法创建.gitignore文件**：
  - 使用命令提示符：`echo. > .gitignore`
  - 或在文件名后加点：`.gitignore.`（系统会自动去掉最后的点）

- **文件不生效**：
  - 确认文件名正确（前面有点）
  - 检查文件是否在正确位置
  - 重启GitHub Desktop

## 🖥️ GitHub桌面版设置

### 1. GitHub Desktop初始配置

#### 1.1 首次启动和登录

> **💡 提示**: 以下步骤适用于官方英文版和中文汉化版，中文版的界面文字会显示为中文。

1. **启动GitHub Desktop**
   - 双击桌面图标或从开始菜单启动
   - 等待应用程序完全加载

2. **登录GitHub账户**

   **官方英文版步骤**：
   ```
   1. 点击 "Sign in to GitHub.com" 按钮
   2. 浏览器会自动打开GitHub登录页面
   3. 输入您的GitHub用户名和密码
   4. 点击 "Sign in"
   5. 如果启用了两步验证，输入验证码
   6. 点击 "Authorize desktop" 授权GitHub Desktop
   7. 返回GitHub Desktop，确认登录成功
   ```

   **中文汉化版步骤**：
   ```
   1. 点击 "登录到GitHub.com" 按钮
   2. 浏览器会自动打开GitHub登录页面
   3. 输入您的GitHub用户名和密码
   4. 点击 "登录"
   5. 如果启用了两步验证，输入验证码
   6. 点击 "授权桌面应用" 授权GitHub Desktop
   7. 返回GitHub Desktop，确认登录成功
   ```

3. **验证登录状态**
   - 在GitHub Desktop界面右上角应显示您的头像
   - 点击头像可以看到账户信息
   - 中文版会显示中文的账户信息

#### 1.2 配置用户信息

1. **打开设置界面**

   **官方英文版**:
   - **Windows用户**: 点击 `File → Options`
   - **Mac用户**: 点击 `GitHub Desktop → Preferences`
   - 或使用快捷键 `Ctrl+,` (Windows) / `Cmd+,` (Mac)

   **中文汉化版**:
   - **Windows用户**: 点击 `文件 → 选项`
   - **Mac用户**: 点击 `GitHub Desktop → 偏好设置`
   - 或使用快捷键 `Ctrl+,` (Windows) / `Cmd+,` (Mac)

2. **配置账户信息**

   **官方英文版**:
   - 选择 **"Accounts"** 选项卡
   - 确认GitHub账户已正确显示
   - 检查账户状态为"Signed in"

   **中文汉化版**:
   - 选择 **"账户"** 选项卡
   - 确认GitHub账户已正确显示
   - 检查账户状态为"已登录"

3. **配置Git信息**

   **官方英文版**:
   - 选择 **"Git"** 选项卡
   - 设置以下信息：
     ```
     Name: 输入您的真实姓名或昵称
     Email: 输入GitHub注册时使用的邮箱地址
     ```

   **中文汉化版**:
   - 选择 **"Git"** 选项卡
   - 设置以下信息：
     ```
     姓名: 输入您的真实姓名或昵称
     邮箱: 输入GitHub注册时使用的邮箱地址
     ```

   - 这些信息会出现在每次提交的记录中

#### 1.3 高级设置配置

1. **外观设置**

   **官方英文版**:
   - 选择 **"Appearance"** 选项卡
   - 选择主题：Light（浅色）或 Dark（深色）
   - 根据个人喜好调整

   **中文汉化版**:
   - 选择 **"外观"** 选项卡
   - 选择主题：浅色 或 深色
   - 根据个人喜好调整

2. **集成设置**

   **官方英文版**:
   - 选择 **"Integrations"** 选项卡
   - 配置默认编辑器（推荐Visual Studio Code）
   - 配置默认Shell（通常保持默认即可）

   **中文汉化版**:
   - 选择 **"集成"** 选项卡
   - 配置默认编辑器（推荐Visual Studio Code）
   - 配置默认终端（通常保持默认即可）

3. **高级设置**

   **官方英文版**:
   - 选择 **"Advanced"** 选项卡
   - 设置使用情况统计（可选）
   - 配置代理设置（如果需要）

   **中文汉化版**:
   - 选择 **"高级"** 选项卡
   - 设置使用情况统计（可选）
   - 配置代理设置（如果需要）

### 2. GitHub Desktop界面介绍

#### 2.1 主界面布局

**官方英文版界面**:
```
GitHub Desktop界面说明：
┌─────────────────────────────────────────┐
│ 菜单栏 (File, Edit, View, Repository...) │
├─────────────────────────────────────────┤
│ 工具栏 (Current Repository, Branch...)   │
├─────────────────────────────────────────┤
│ 左侧面板：文件变更列表                    │
│ 右侧面板：文件差异显示                    │
├─────────────────────────────────────────┤
│ 底部：提交信息输入区域                    │
└─────────────────────────────────────────┘
```

**中文汉化版界面**:
```
GitHub Desktop界面说明：
┌─────────────────────────────────────────┐
│ 菜单栏 (文件, 编辑, 查看, 仓库...)        │
├─────────────────────────────────────────┤
│ 工具栏 (当前仓库, 分支...)               │
├─────────────────────────────────────────┤
│ 左侧面板：文件变更列表                    │
│ 右侧面板：文件差异显示                    │
├─────────────────────────────────────────┤
│ 底部：提交信息输入区域                    │
└─────────────────────────────────────────┘
```

#### 2.2 重要功能按钮对照

| 功能 | 英文版 | 中文版 | 说明 |
|------|--------|--------|------|
| 当前仓库 | Current Repository | 当前仓库 | 显示当前仓库，点击可切换仓库 |
| 当前分支 | Current Branch | 当前分支 | 显示当前分支，点击可切换分支 |
| 获取更新 | Fetch origin | 获取源 | 从远程仓库获取最新更新 |
| 推送 | Push origin | 推送到源 | 将本地提交推送到远程仓库 |
| 拉取 | Pull origin | 拉取源 | 拉取并合并远程更新 |
| 提交 | Commit to main | 提交到主分支 | 将更改提交到当前分支 |
| 发布仓库 | Publish repository | 发布仓库 | 将本地仓库发布到GitHub |

#### 2.3 快捷键参考
```
常用快捷键（两个版本通用）：
Ctrl+N (Cmd+N)     : 创建新仓库
Ctrl+O (Cmd+O)     : 打开仓库
Ctrl+Shift+A       : 添加本地仓库
Ctrl+Enter         : 提交更改
Ctrl+Shift+P       : 推送到远程
Ctrl+Shift+F       : 从远程获取
Ctrl+T (Cmd+T)     : 切换分支
```

#### 2.4 版本选择建议

**选择官方英文版的情况**:
- ✅ 有一定英文基础
- ✅ 希望获得最新功能
- ✅ 需要官方技术支持
- ✅ 团队使用英文版

**选择中文汉化版的情况**:
- ✅ 英文水平有限
- ✅ 初次使用Git工具
- ✅ 希望降低学习门槛
- ✅ 更注重操作便利性

> **💡 提示**: 无论选择哪个版本，功能都是完全一样的，只是界面语言不同。您可以根据自己的情况选择最适合的版本。

## 📤 创建仓库并上传

### 1. 创建本地Git仓库

#### 1.1 添加Unity工程到GitHub Desktop
1. **打开GitHub Desktop**
   - 确保已经登录并配置完成
   - 界面应显示"Let's get started!"或仓库列表

2. **添加本地仓库**
   ```
   方法一：使用菜单
   1. 点击 "File" → "Add local repository"
   2. 点击 "Choose..." 按钮
   3. 浏览并选择您的Unity工程文件夹
   4. 点击 "Select Folder"

   方法二：拖拽添加
   1. 直接将Unity工程文件夹拖拽到GitHub Desktop窗口
   ```

3. **处理Git仓库检测**
   - 如果显示"This directory does not appear to be a Git repository"
   - 点击 **"create a repository"** 链接
   - 这是正常情况，因为Unity工程默认不包含Git仓库

#### 1.2 初始化Git仓库
1. **填写仓库信息**
   ```
   Create a New Repository对话框：

   Name: [输入仓库名称]
   - 建议与Unity工程名称相同
   - 使用英文和数字，避免特殊字符
   - 例如：MyUnityGame, PlatformerGame2D

   Description: [输入项目描述]
   - 简短描述项目内容（可选）
   - 例如：A 2D platformer game built with Unity

   Local path: [确认路径正确]
   - 应该指向您的Unity工程根目录
   - 包含Assets、ProjectSettings等文件夹的目录

   Initialize this repository with a README: ✓
   - 建议勾选，会创建README.md文件

   Git ignore: Unity
   - 选择Unity模板，自动生成适合Unity的.gitignore文件
   - 如果没有此选项，可以手动创建（参考前面章节）

   License: [选择许可证]
   - 根据项目性质选择合适的许可证
   - 详细说明见下方许可证部分
   ```

2. **许可证选择指南**

#### 2.1 什么是许可证？
许可证（License）是一个法律文档，规定了其他人如何使用、修改和分发您的代码。选择合适的许可证对于开源项目非常重要。

#### 2.2 常见许可证类型

**🔓 宽松许可证（推荐用于游戏项目）**

| 许可证 | 特点 | 适用场景 | 限制 |
|--------|------|----------|------|
| **MIT License** | 最宽松，使用最广泛 | 个人项目、学习项目、商业友好 | 几乎无限制，只需保留版权声明 |
| **Apache 2.0** | 宽松，提供专利保护 | 大型项目、企业项目 | 需要保留版权和许可证声明 |
| **BSD 3-Clause** | 简单宽松 | 学术项目、小型项目 | 不能使用作者名字做推广 |

**🔒 Copyleft许可证（要求开源）**

| 许可证 | 特点 | 适用场景 | 限制 |
|--------|------|----------|------|
| **GPL v3** | 强制开源 | 完全开源项目 | 衍生作品必须开源 |
| **LGPL v3** | 部分强制开源 | 库和组件 | 修改部分必须开源 |

**🚫 限制性许可证**

| 许可证 | 特点 | 适用场景 | 限制 |
|--------|------|----------|------|
| **All Rights Reserved** | 完全保留权利 | 商业项目、私有项目 | 他人不能使用、修改或分发 |

#### 2.3 Unity游戏项目推荐

**🎮 个人学习项目**
```
推荐：MIT License
理由：
✅ 简单易懂
✅ 允许他人学习和参考
✅ 对未来商业化友好
✅ 社区接受度高
```

**🎮 开源游戏项目**
```
推荐：MIT License 或 Apache 2.0
理由：
✅ 鼓励社区贡献
✅ 允许商业使用
✅ 保护原作者权益
✅ 便于项目推广
```

**🎮 商业游戏项目**
```
推荐：All Rights Reserved 或不选择许可证
理由：
✅ 完全控制代码使用权
✅ 保护商业利益
✅ 避免代码泄露
✅ 符合商业开发需求
```

**🎮 教育项目**
```
推荐：MIT License 或 Apache 2.0
理由：
✅ 便于教学分享
✅ 学生可以学习和修改
✅ 促进知识传播
✅ 建立开源社区
```

#### 2.4 许可证选择建议

**选择流程图**：
```
开始
  ↓
是否希望完全保护代码？
  ├─ 是 → All Rights Reserved
  └─ 否 ↓
是否希望衍生作品也开源？
  ├─ 是 → GPL v3
  └─ 否 ↓
是否需要专利保护？
  ├─ 是 → Apache 2.0
  └─ 否 → MIT License
```

**常见误区**：
```
❌ 不选择许可证 = 完全保护
   实际：法律上可能存在争议

❌ 开源 = 免费
   实际：开源项目也可以商业化

❌ MIT许可证 = 完全免费使用
   实际：需要保留版权声明

❌ 选择许可证后不能更改
   实际：作为原作者可以更改许可证
```

3. **创建仓库**
   - 检查所有信息无误后
   - 确认许可证选择合适
   - 点击 **"Create Repository"** 按钮
   - 等待仓库创建完成

#### 1.3 验证仓库创建
1. **检查GitHub Desktop界面**
   - 左上角应显示您的仓库名称
   - 当前分支应显示为"main"或"master"
   - 左侧面板会显示检测到的文件变更

2. **检查文件状态**
   - 左侧会列出所有Unity工程文件
   - 文件前面有绿色"+"号表示新增文件
   - 应该能看到Assets、ProjectSettings等文件夹

### 2. 首次提交（Commit）

#### 2.1 理解提交概念
- **提交（Commit）**: 将文件变更保存到本地Git仓库的操作
- **暂存（Stage）**: 选择哪些文件包含在本次提交中
- **提交信息**: 描述本次提交内容的文本

#### 2.2 检查要提交的文件
1. **查看文件列表**
   - 在左侧面板查看所有变更文件
   - 确认包含了必要的Unity文件
   - 确认.gitignore文件已生效（Library、Temp等文件夹不应出现）

2. **选择要提交的文件**
   - 默认情况下所有文件都会被选中
   - 可以取消勾选不需要提交的文件
   - 建议首次提交包含所有必要文件

#### 2.3 编写提交信息
1. **填写提交摘要**
   ```
   Summary（必填）：
   Initial Unity project commit

   或者更具体的描述：
   Add Unity 2D platformer game project
   ```

2. **填写详细描述（可选）**
   ```
   Description：
   - Added Unity project structure
   - Configured version control settings
   - Added .gitignore for Unity
   - Initial scene and basic game objects
   ```

#### 2.4 执行提交
1. **提交到本地仓库**
   - 确认提交信息无误
   - 点击 **"Commit to main"** 按钮
   - 等待提交完成

2. **验证提交成功**
   - 左侧文件列表应该清空
   - 界面显示"No local changes"
   - 历史记录中应该出现您的提交

### 3. 发布到GitHub远程仓库

#### 3.1 发布仓库
1. **点击发布按钮**
   - 在GitHub Desktop顶部找到 **"Publish repository"** 按钮
   - 点击该按钮

2. **配置远程仓库设置**
   ```
   Publish Repository对话框：

   Name: [确认仓库名称]
   - 通常与本地仓库名称相同
   - 这将是GitHub上的仓库名称

   Description: [确认描述]
   - 与本地仓库描述相同

   Keep this code private: [选择可见性]
   - 勾选：创建私有仓库（只有您能看到）
   - 不勾选：创建公开仓库（所有人都能看到）

   Organization: [选择组织]
   - 通常选择您的个人账户
   - 如果属于组织，可以选择组织账户
   ```

#### 3.2 仓库可见性选择指南

**🔒 私有仓库（Private Repository）**
```
适用场景：
✅ 商业游戏项目
✅ 个人练习项目
✅ 包含敏感信息的项目
✅ 未完成的项目
✅ 团队内部项目

优点：
✅ 完全控制访问权限
✅ 保护知识产权
✅ 避免代码泄露
✅ 可以邀请特定成员协作

限制：
❌ 无法获得社区贡献
❌ 不利于个人技术展示
❌ 免费账户有私有仓库数量限制
```

**🌍 公开仓库（Public Repository）**
```
适用场景：
✅ 开源游戏项目
✅ 学习和教育项目
✅ 技术演示项目
✅ 社区贡献项目
✅ 个人作品集展示

优点：
✅ 获得社区反馈和贡献
✅ 提升个人技术影响力
✅ 便于技术交流和学习
✅ 无数量限制

注意事项：
⚠️ 代码完全公开
⚠️ 需要选择合适的许可证
⚠️ 可能被他人复制使用
⚠️ 需要维护代码质量
```

#### 3.3 许可证与可见性的关系

**私有仓库 + 任何许可证**
```
- 许可证主要影响未来开源时的规则
- 即使设置了开源许可证，私有仓库仍然是私有的
- 建议：可以先选择宽松许可证，为将来开源做准备
```

**公开仓库 + 开源许可证**
```
- 许可证立即生效，规定他人如何使用您的代码
- 必须选择合适的许可证
- 建议：Unity游戏项目推荐MIT或Apache 2.0
```

**公开仓库 + 无许可证**
```
⚠️ 不推荐：法律上他人无法合法使用您的代码
⚠️ 可能导致：潜在的法律纠纷
⚠️ 建议：总是为公开仓库选择明确的许可证
```

3. **发布到GitHub**
   - 确认所有设置正确
   - 确认许可证和可见性选择合适
   - 点击 **"Publish Repository"** 按钮
   - 等待上传完成（可能需要几分钟，取决于项目大小）

#### 3.2 验证发布成功
1. **检查GitHub Desktop状态**
   - "Publish repository"按钮应该变为"Fetch origin"
   - 顶部应显示远程仓库信息

2. **访问GitHub网站验证**
   - 打开浏览器访问 [github.com](https://github.com)
   - 登录您的账户
   - 在仓库列表中应该能看到新创建的仓库
   - 点击仓库名称查看内容

## 📚 版本控制最佳实践

### 1. 提交频率和时机

#### 1.1 何时进行提交
```
推荐提交时机：
✅ 完成一个功能特性
✅ 修复一个bug
✅ 添加新的游戏对象或场景
✅ 修改重要配置
✅ 每日工作结束前
✅ 重要里程碑节点

❌ 避免的提交时机：
❌ 代码无法编译时
❌ 游戏无法正常运行时
❌ 包含临时测试代码时
❌ 文件过于庞大时（超过100MB）
```

#### 1.2 提交频率建议
- **小型项目**：每天1-3次提交
- **中型项目**：每完成一个小功能就提交
- **团队协作**：至少每天提交一次
- **个人项目**：根据进度灵活调整

### 2. 提交信息规范

#### 2.1 提交信息格式
```
标准格式：
类型(范围): 简短描述

详细描述（可选）

示例：
feat(player): 添加玩家跳跃功能
fix(enemy): 修复敌人AI路径查找bug
docs: 更新项目README文档
style(ui): 调整主菜单界面布局
```

#### 2.2 提交类型说明
```
feat:     新功能
fix:      bug修复
docs:     文档更新
style:    代码格式调整（不影响功能）
refactor: 代码重构
test:     添加或修改测试
chore:    构建过程或辅助工具的变动
perf:     性能优化
```

#### 2.3 Unity特定提交示例
```
Unity项目常见提交信息：
feat(scene): 添加新的游戏关卡
feat(player): 实现玩家攻击系统
fix(audio): 修复背景音乐循环问题
fix(physics): 解决碰撞检测异常
style(ui): 更新游戏界面设计
docs: 添加游戏操作说明
chore: 更新Unity版本到2022.3 LTS
```

### 3. 分支管理策略

#### 3.1 基础分支结构
```
分支层次结构：
main (或 master)
├── develop
├── feature/player-movement
├── feature/enemy-ai
├── hotfix/critical-bug
└── release/v1.0
```

#### 3.2 分支类型说明
1. **main/master分支**
   - 稳定的生产版本
   - 只包含经过测试的代码
   - 每次合并都应该是一个可发布的版本

2. **develop分支**
   - 开发主分支
   - 包含最新的开发进度
   - 功能开发完成后合并到此分支

3. **feature分支**
   - 功能开发分支
   - 从develop分支创建
   - 命名格式：`feature/功能名称`
   - 完成后合并回develop分支

4. **hotfix分支**
   - 紧急修复分支
   - 从main分支创建
   - 修复完成后同时合并到main和develop

#### 3.3 GitHub Desktop分支操作
1. **创建新分支**
   ```
   步骤：
   1. 点击顶部的 "Current Branch"
   2. 点击 "New Branch"
   3. 输入分支名称（如：feature/player-jump）
   4. 选择基于哪个分支创建
   5. 点击 "Create Branch"
   ```

2. **切换分支**
   ```
   步骤：
   1. 点击顶部的 "Current Branch"
   2. 从列表中选择要切换的分支
   3. 点击分支名称完成切换
   ```

3. **合并分支**
   ```
   步骤：
   1. 切换到目标分支（如develop）
   2. 点击 "Branch" → "Merge into current branch"
   3. 选择要合并的分支
   4. 点击 "Merge"
   ```

### 4. 文件管理最佳实践

#### 4.1 Unity资源组织
```
推荐的Assets文件夹结构：
Assets/
├── Scripts/           # 脚本文件
├── Scenes/           # 场景文件
├── Prefabs/          # 预制体
├── Materials/        # 材质
├── Textures/         # 贴图
├── Audio/            # 音频文件
├── Animations/       # 动画文件
├── Fonts/            # 字体文件
└── Plugins/          # 插件
```

#### 4.2 命名规范
```
文件命名建议：
✅ 使用英文命名
✅ 使用PascalCase（首字母大写）
✅ 名称要有意义
✅ 避免特殊字符和空格

示例：
PlayerController.cs
MainMenuScene.unity
PlayerJumpAnimation.anim
BackgroundMusic.mp3
```

## 🔧 常见问题解决

### 1. 文件大小相关问题

#### 1.1 文件过大无法上传
**问题症状**：
- 上传时提示文件过大
- GitHub限制单个文件最大100MB
- 推送失败或速度极慢

**解决方案**：
1. **检查大文件**
   ```
   常见的Unity大文件：
   - .fbx 模型文件
   - .png/.jpg 高分辨率贴图
   - .mp3/.wav 音频文件
   - .mp4 视频文件
   - .unitypackage 包文件
   ```

2. **使用Git LFS（大文件存储）**
   ```
   在Unity工程根目录创建 .gitattributes 文件：

   # 3D模型文件
   *.fbx filter=lfs diff=lfs merge=lfs -text
   *.obj filter=lfs diff=lfs merge=lfs -text

   # 贴图文件
   *.png filter=lfs diff=lfs merge=lfs -text
   *.jpg filter=lfs diff=lfs merge=lfs -text
   *.tga filter=lfs diff=lfs merge=lfs -text

   # 音频文件
   *.mp3 filter=lfs diff=lfs merge=lfs -text
   *.wav filter=lfs diff=lfs merge=lfs -text
   *.ogg filter=lfs diff=lfs merge=lfs -text

   # 视频文件
   *.mp4 filter=lfs diff=lfs merge=lfs -text
   *.mov filter=lfs diff=lfs merge=lfs -text
   ```

3. **压缩和优化资源**
   - 在Unity中压缩贴图
   - 降低音频质量
   - 使用更高效的文件格式

#### 1.2 仓库体积过大
**解决方案**：
- 定期清理不需要的资源
- 使用.gitignore忽略临时文件
- 考虑将大型资源存储在外部

### 2. 同步和冲突问题

#### 2.1 合并冲突解决
**问题症状**：
- 推送时提示有冲突
- GitHub Desktop显示冲突文件
- 无法自动合并

**解决步骤**：
1. **获取最新更改**
   ```
   步骤：
   1. 点击 "Fetch origin" 获取远程更新
   2. 如果有冲突，GitHub Desktop会提示
   3. 点击 "View conflicts" 查看冲突文件
   ```

2. **手动解决冲突**
   ```
   冲突标记说明：
   <<<<<<< HEAD
   您的更改
   =======
   远程更改
   >>>>>>> branch-name

   解决方法：
   1. 打开冲突文件
   2. 删除冲突标记
   3. 保留需要的内容
   4. 保存文件
   ```

3. **完成合并**
   ```
   步骤：
   1. 解决所有冲突文件
   2. 在GitHub Desktop中标记为已解决
   3. 提交合并结果
   4. 推送到远程仓库
   ```

#### 2.2 Unity特定冲突处理
**场景文件冲突**：
- Unity场景文件冲突较难手动解决
- 建议使用Unity的Smart Merge工具
- 或者重新创建冲突的场景部分

**项目设置冲突**：
- ProjectSettings文件夹中的冲突
- 通常选择最新的设置
- 必要时重新配置项目设置

### 3. 权限和访问问题

#### 3.1 推送权限被拒绝
**问题症状**：
- 推送时提示"Permission denied"
- 无法访问远程仓库

**解决方案**：
1. **检查登录状态**
   - 确认GitHub Desktop已正确登录
   - 重新登录GitHub账户

2. **检查仓库权限**
   - 确认您有仓库的写入权限
   - 如果是组织仓库，联系管理员

3. **更新认证信息**
   - 在GitHub Desktop中重新授权
   - 检查GitHub个人访问令牌

#### 3.2 仓库不存在或无法访问
**解决方案**：
- 检查仓库URL是否正确
- 确认仓库没有被删除
- 检查网络连接

### 4. Unity特定问题

#### 4.1 .meta文件问题
**问题症状**：
- 资源引用丢失
- Unity报告missing references

**解决方案**：
1. **确保.meta文件被跟踪**
   - 检查.gitignore没有忽略.meta文件
   - 确保Version Control Mode设置正确

2. **恢复丢失的.meta文件**
   - 从其他分支或提交中恢复
   - 重新导入受影响的资源

#### 4.2 Library文件夹问题
**问题症状**：
- Library文件夹被意外提交
- 仓库体积异常庞大

**解决方案**：
1. **从版本控制中移除**
   ```
   在Git命令行中执行：
   git rm -r --cached Library/
   git commit -m "Remove Library folder from tracking"
   ```

2. **更新.gitignore**
   - 确保.gitignore包含Library/
   - 提交.gitignore更改

#### 4.3 Unity版本兼容性
**问题症状**：
- 项目无法在不同Unity版本间正常工作
- 出现版本相关错误

**解决方案**：
- 在README中明确Unity版本要求
- 使用Unity LTS版本保证稳定性
- 团队成员使用相同的Unity版本

## 📖 进阶操作指南

### 1. 日常工作流程

#### 1.1 标准工作流程
```
每日开发流程：
1. 🌅 开始工作
   └── Fetch origin (获取最新更新)

2. 💻 开发过程
   ├── 编写代码
   ├── 测试功能
   └── Commit changes (提交更改)

3. 🌙 结束工作
   └── Push origin (推送到远程)
```

#### 1.2 详细操作步骤
1. **开始工作前**
   ```
   步骤：
   1. 打开GitHub Desktop
   2. 选择正确的仓库
   3. 点击 "Fetch origin" 获取最新代码
   4. 如有更新，点击 "Pull origin" 拉取更改
   5. 打开Unity编辑器开始工作
   ```

2. **开发过程中**
   ```
   建议频率：
   - 每完成一个小功能：提交一次
   - 每修复一个bug：提交一次
   - 每天至少：提交一次
   - 重要节点：立即提交
   ```

3. **结束工作时**
   ```
   步骤：
   1. 保存Unity项目
   2. 在GitHub Desktop中查看更改
   3. 编写清晰的提交信息
   4. 提交到本地仓库
   5. 推送到远程仓库
   ```

### 2. 团队协作进阶

#### 2.1 Pull Request工作流
1. **创建Pull Request**
   ```
   步骤：
   1. 在feature分支完成开发
   2. 推送分支到GitHub
   3. 在GitHub网站创建Pull Request
   4. 填写PR描述和相关信息
   5. 请求团队成员审查
   ```

2. **代码审查流程**
   ```
   审查要点：
   ✅ 代码质量和规范
   ✅ 功能是否正确实现
   ✅ 是否有潜在bug
   ✅ 性能影响
   ✅ 文档是否完整
   ```

#### 2.2 Issue管理
1. **创建Issue**
   ```
   Issue类型：
   🐛 Bug Report - 报告bug
   ✨ Feature Request - 功能请求
   📚 Documentation - 文档改进
   ❓ Question - 问题咨询
   ```

2. **Issue模板示例**
   ```markdown
   ## Bug描述
   简要描述遇到的问题

   ## 复现步骤
   1. 打开游戏
   2. 点击开始按钮
   3. 进入第一关
   4. 玩家无法移动

   ## 预期行为
   玩家应该能够正常移动

   ## 环境信息
   - Unity版本：2022.3.0f1
   - 平台：Windows 10
   - 设备：PC
   ```

#### 2.3 项目管理
1. **使用GitHub Projects**
   - 创建项目看板
   - 设置不同状态列（To Do, In Progress, Done）
   - 将Issues和PR关联到项目

2. **里程碑管理**
   - 设置版本里程碑
   - 将相关Issues分配到里程碑
   - 跟踪开发进度

### 3. 高级Git操作

#### 3.1 标签和发布
1. **创建标签**
   ```
   用途：
   - 标记重要版本
   - 便于版本回滚
   - 发布管理

   命名规范：
   v1.0.0 - 主要版本
   v1.1.0 - 次要版本
   v1.1.1 - 补丁版本
   ```

2. **创建Release**
   ```
   步骤：
   1. 在GitHub网站进入仓库
   2. 点击 "Releases"
   3. 点击 "Create a new release"
   4. 选择标签或创建新标签
   5. 填写发布说明
   6. 上传构建文件（可选）
   7. 发布Release
   ```

#### 3.2 备份策略
1. **多重备份**
   ```
   备份层次：
   1. 本地Git仓库
   2. GitHub远程仓库
   3. 其他Git托管服务（GitLab, Bitbucket）
   4. 本地文件备份
   ```

2. **自动化备份**
   - 设置GitHub Actions自动备份
   - 定期导出项目文件
   - 云存储同步

### 4. 性能优化

#### 4.1 仓库优化
1. **定期清理**
   ```
   清理内容：
   - 删除不需要的分支
   - 清理大文件历史
   - 压缩Git对象
   ```

2. **LFS优化**
   - 合理使用Git LFS
   - 定期清理LFS缓存
   - 监控LFS存储使用量

#### 4.2 工作流优化
1. **提交优化**
   - 避免过大的提交
   - 合理拆分功能提交
   - 使用有意义的提交信息

2. **分支策略优化**
   - 及时删除已合并分支
   - 保持分支结构清晰
   - 定期同步主分支

## 🎯 总结与检查清单

### 完成检查清单
完成本教程后，您应该能够：

- [ ] ✅ 成功安装并配置GitHub Desktop
- [ ] ✅ 正确配置Unity项目的版本控制设置
- [ ] ✅ 创建适合Unity的.gitignore文件
- [ ] ✅ 将Unity项目初始化为Git仓库
- [ ] ✅ 进行首次提交并推送到GitHub
- [ ] ✅ 理解基本的Git工作流程
- [ ] ✅ 掌握分支的创建和管理
- [ ] ✅ 能够解决常见的版本控制问题
- [ ] ✅ 建立良好的提交习惯和规范

### 关键要点回顾

1. **配置要点**
   - Unity版本控制模式：Visible Meta Files
   - 资源序列化模式：Force Text
   - 正确的.gitignore配置

2. **工作流要点**
   - 定期提交和推送
   - 清晰的提交信息
   - 合理的分支管理
   - 及时解决冲突

3. **团队协作要点**
   - 使用Pull Request进行代码审查
   - 通过Issues跟踪问题和功能
   - 保持良好的沟通和文档

### 下一步建议

1. **深入学习**
   - 学习更多Git命令
   - 了解GitHub高级功能
   - 掌握Unity协作最佳实践

2. **实践应用**
   - 在实际项目中应用所学知识
   - 与团队成员协作开发
   - 建立项目开发规范

3. **持续改进**
   - 根据项目需求调整工作流
   - 学习新的工具和技术
   - 分享经验和最佳实践

---

**🎉 恭喜！您已经掌握了使用GitHub Desktop管理Unity项目的完整流程。**

通过本教程，您的Unity项目现在拥有了：
- ✨ 完整的版本控制系统
- 🔄 可靠的备份和同步机制
- 👥 支持团队协作的工作流程
- 📈 可追踪的开发历史记录

记住：版本控制是一个持续的过程，需要在实践中不断完善和优化。祝您的Unity开发之路顺利！
