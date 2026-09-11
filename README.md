# fanqiehehe - 番茄小说去广告 + 解锁 SVIP

番茄小说、番茄畅听、红果短剧的 Theos Tweak，去除广告并解锁会员。

## 功能

- ✅ 强制 VIP 状态（永久会员）
- ✅ 移除开屏广告
- ✅ 移除阅读页插广告
- ✅ 移除横幅广告
- ✅ 支持番茄小说、番茄畅听、红果短剧

## 适用版本

- iOS 15.0+
- Bundle ID: `com.dragon.read`（番茄小说）
- Bundle ID: `com.phoenix.video`（红果短剧）
- Bundle ID: `com.fq.music`（番茄畅听）

## 快速开始（GitHub Actions 编译）

### 步骤 1：Fork 本仓库

1. 打开 [https://github.com/new](https://github.com/new)
2. 创建一个新仓库，名称随意（如 `fanqiehehe-custom`）
3. 勾选 "Copy the main branch only"
4. 点击 "Create repository"

### 步骤 2：上传文件

将本仓库的所有文件上传到你的仓库：

```bash
# 克隆你的仓库
git clone https://github.com/YOUR_USERNAME/你的仓库名.git
cd 你的仓库名

# 复制所有文件
cp /path/to/fanqiehehe-tweak/* .
cp /path/to/fanqiehehe-tweak/.github -r .

# 提交并推送
git add .
git commit -m "Initial commit"
git push origin main
```

### 步骤 3：运行 GitHub Actions

1. 打开你的仓库，点击 "Actions" 标签页
2. 点击 "Build fanqiehehe .deb" 工作流
3. 点击 "Run workflow" 按钮
4. 等待 2-3 分钟，编译完成后下载 artifact

### 步骤 4：下载 .deb 文件

在 Actions 运行完成后：
1. 点击最新的运行记录
2. 向下滚动到 "Artifacts" 部分
3. 下载 `fanqiehehe-deb.zip`
4. 解压后得到 `.deb` 文件

## iPhone 安装步骤

### 需要的工具

| 工具 | 用途 | 下载地址 |
|------|------|----------|
| Sideloadly | IPA 签名安装 | [sideloadly.io](https://sideloadly.io) |
| iDevice Toolkit | Tweak 注入（iOS 26 兼容）| 项目文件夹中的 `iDeviceToolKit-v2.0.1.ipa` |
| Asspp | 下载官方 IPA | 项目文件夹中的 `Asspp.ipa` |

### 详细步骤

#### 1. 安装 iDevice Toolkit

1. 用 Sideloadly 将 `iDeviceToolKit-v2.0.1.ipa` 安装到 iPhone
2. 在 iPhone 上：设置 → 通用 → VPN与设备管理 → 信任你的 Apple ID

#### 2. 下载官方番茄小说 IPA

1. 用 Sideloadly 安装 `Asspp.ipa`
2. 打开 Asspp，登录 Apple ID
3. 搜索"番茄免费小说"，下载最新版
4. 保存 IPA 文件到电脑

#### 3. 注入 Tweak

1. 打开 iDevice Toolkit
2. 选择 "Inject Tweak" 功能
3. 选择下载的番茄小说 IPA
4. 选择编译好的 `fanqiehehe.deb`
5. 点击 "Inject"，等待完成
6. 用 Sideloadly 安装注入后的 IPA

#### 4. 完成！

打开番茄小说，享受无广告 + SVIP 体验！

## 文件说明

| 文件 | 说明 |
|------|------|
| `Tweak.x` | Hook 源代码（Objective-C） |
| `Makefile` | 编译配置 |
| `control` | deb 包控制文件 |
| `fanqiehehe.plist` | Ellekit 注入配置 |
| `.github/workflows/build.yml` | GitHub Actions 编译配置 |

## 注意事项

- ⚠️ 仅用于学习研究，请勿用于商业用途
- ⚠️ 使用修改版 App 可能违反用户协议
- ⚠️ 建议使用小号测试
- ⚠️ 签名每 7 天过期，需重新安装
- ⚠️ App 更新后可能需要重新编译 Tweak

## 相关链接

- 原作者 Telegram：https://t.me/iparxwy
- Theos 项目：https://github.com/theos/theos

## 许可证

MIT License
