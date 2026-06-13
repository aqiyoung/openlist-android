# 三页云盘 v0.1.1-beta (build 3) Release Notes

## 1️⃣ 品牌升级
- **APP 名称**: `OpenList` → **三页云盘**（中文优先，跟"三页札记"公众号呼应）
- **APP 副标题**: 三页 · 云盘聚合
- **APP 图标升级 (icon v5)**: cairosvg 矢量渲染 res.oplist.org 官方 logo
  - sky-400 #38BDF8 + teal-200 #99F6E4
  - 22% 圆角 + 5 mipmap 尺寸 + round launcher
  - 修复 cairosvg 不解析 CSS 变量 → 字面色展开

## 2️⃣ 构建类型 (Build Types)
- `debug` - applicationId `com.threel.openlist.debug`, versionName 后缀 `-debug`（开发联调用）
- `beta` - applicationId `com.threel.openlist.beta`, versionName 后缀 `-beta`（老板手机直装 / 内部测试）
- `release` - applicationId `com.threel.openlist`, isMinifyEnabled true（生产发布，待加签名）

**3 个 applicationId 可并存**（老板手机能装 debug + beta + release 各一份）

## 3️⃣ 版本迭代支持
- **versionCode 2 → 3**
- **versionName 0.1.0 → 0.1.1**
- **CHANGELOG.md** 项目内（详细迭代记录）
- **AppConfig.kt** 工具类（versionName/Code/buildType 真实值，供 UI 显示）
- **AboutScreen.kt** 新页面：
  - 品牌大字 + 副标题 + 老板家出品签名
  - 应用名称 / 英文名 / 完整版本 / 构建类型 / Package
  - 版本更新日志链接
  - 检查更新链接
- **FileBrowserScreen** TopAppBar 加 "关于" 入口按钮（Info 图标）

## 4️⃣ 默认 server URL
- `https://fn.threel.site`（域名，非 IP）
- `TokenStore.DEFAULT_SERVER` 已配置

## 5️⃣ 字符串资源扩展
- `app_name` → "三页云盘"
- `app_name_en` → "OpenList"
- `app_subtitle` → "三页 · 云盘聚合"
- `app_version_format` → "v%1$s (build %2$d)"
- `changelog_url` → "https://fn.threel.site/api/openlist-android/changelog.json"
- `update_check_url` → "https://fn.threel.site/api/openlist-android/latest.json"
- `about_brand_line` → "「三页」出品 · 聚合你的所有云盘"
