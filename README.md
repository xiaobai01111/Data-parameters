# Data-parameters

SSMT4 的数据参数仓库（与主程序代码解耦）。

## 目录结构

- `catalogs/`
  - `game_catalog.seed.json`: 游戏 identity/preset（包含 launcher API、下载服务器、遥测配置）
  - `proton_catalog.seed.json`: Proton 全量种子（兼容回退）
  - `dxvk_catalog.json`: DXVK 全量种子（兼容回退）
- `games/`
  - `<GameName>/Config.json`
  - `<GameName>/Icon.png`
- `proton/`
  - `families.json`: 家族定义
  - `<familyKey>/sources.json`: 每个家族独立源配置（官方/实验/GE/DW/CachyOS/EM/Sarek/TKG/Custom）
- `dxvk/`
  - `index.json`: variant 索引
  - `dxvk.json`
  - `gplasync.json`

## 说明

主项目运行时优先读取模块化目录（`proton/` 与 `dxvk/`），`catalogs/*.json` 仅作兼容回退。
