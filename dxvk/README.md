# DXVK Modules

- `index.json`: DXVK 变体索引（模块开关 + 文件路径）。
- `<variant>.json`: 单个变体的来源定义（provider/repo/pattern/template）。

当前模块化变体：

- `dxvk`（官方）
- `gplasync`
- `async`
- `sarek`
- `sarekasync`

运行时加载顺序：

1. 优先读取本目录模块化结构。
2. 兼容回退 `catalogs/dxvk_catalog.json`。
3. 最后回退内置默认配置。
