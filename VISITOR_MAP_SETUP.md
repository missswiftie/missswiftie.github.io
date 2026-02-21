# 访问地图设置说明

## 方案 1：使用 ClustrMaps（推荐，最简单）

### 步骤：

1. **注册 ClustrMaps 账户**
   - 访问：https://clustrmaps.com/
   - 注册免费账户

2. **添加你的网站**
   - 登录后，添加你的网站 URL（如：https://missswiftie.github.io）
   - 获取你的网站标识符（Site Identifier）

3. **更新 HTML 代码**
   - 打开 `_layouts/default.html`
   - 找到第 231 行的代码：
     ```html
     <script type='text/javascript' id='clustrmaps' src='//cdn.clustrmaps.com/map_v2.js?cl=ffffff&w=600&t=tt&d=YOUR_SITE_IDENTIFIER&co=2d78ad&cmo=ff5353&cmn=ff5353&ct=ffffff'></script>
     ```
   - 将 `YOUR_SITE_IDENTIFIER` 替换为你从 ClustrMaps 获取的实际标识符

4. **自定义样式（可选）**
   - `cl=ffffff` - 地图背景色（白色）
   - `w=600` - 地图宽度（像素）
   - `co=2d78ad` - 国家颜色
   - `cmo=ff5353` - 访问点颜色
   - `ct=ffffff` - 文本颜色

---

## 方案 2：使用 Google Analytics + 自定义地图

如果你已经使用 Google Analytics，可以：

1. **在 Google Analytics 中查看地理位置数据**
   - 登录 Google Analytics
   - 进入 "Reports" > "Audience" > "Geo" > "Location"
   - 导出访问数据

2. **使用 Leaflet.js 创建自定义地图**
   - 需要手动集成 Leaflet.js 库
   - 需要将访问数据转换为地图标记点
   - 更灵活但需要更多开发工作

---

## 方案 3：使用 Flag Counter（简单但功能有限）

如果你只需要显示访问者国家，可以使用 Flag Counter：

1. 访问：https://flagcounter.com/
2. 获取嵌入代码
3. 替换 ClustrMaps 代码

---

## 当前状态

目前 HTML 中已添加了 ClustrMaps 的代码框架，但需要：
- 注册 ClustrMaps 账户
- 获取网站标识符
- 替换 `YOUR_SITE_IDENTIFIER`

完成这些步骤后，地图会自动开始追踪访问者位置并在世界地图上显示。

