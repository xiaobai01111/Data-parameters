# DXVK Modules

- `index.json`: variant 索引（id -> 文件路径）
- `<variant>.json`: 单个 variant 的源定义（如 `dxvk.json`、`gplasync.json`）

程序运行时优先读取本目录的模块化结构，`catalogs/dxvk_catalog.json` 作为兼容回退。
