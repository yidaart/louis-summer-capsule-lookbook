# Louis Outfit System

Louis 个人穿搭管理系统 v1。

- `index.html`: GitHub Pages 页面
- `data/items.json`: 单品库
- `data/looks.json`: Look 组合库
- `assets/louis-summer-looks/`: 72 张夏日穿搭插画图

## 新增单品

v1 暂不接后台。新增单品时，先在 `data/items.json` 增加一条记录：

- `id`: 单品唯一 ID
- `name`: 单品名称
- `category`: `tops` / `outerwear` / `bottoms` / `shoes` / `bags` / `accessories`
- `season`: 例如 `["summer"]`，后续秋装用 `autumn`，冬装用 `winter`
- `colors`: 颜色标签
- `weatherTags`: 适合天气
- `temperatureC`: 适合温度区间
- `enabled`: 是否启用

## 新增 Look

在 `data/looks.json` 增加一条 Look，引用 `items.json` 里的单品 ID，并把图片放到 `assets/` 下。

后续如果需要手机端新增、登录、图片上传和多设备同步，再把 JSON 数据源替换为后台数据库。
