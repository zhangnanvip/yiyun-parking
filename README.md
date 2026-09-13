# 壹云花园车位地图

纯静态网页，包含高清原图、565 个车位标注、Leaflet 本地依赖及模拟价格/销售状态。

## GitHub Pages 发布

将文件放在仓库根目录。打开 Settings → Pages，选择 Deploy from a branch，然后选择 main 分支和 / (root)，保存。

官方说明：https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site

## 本地查看

在此目录运行 `python -m http.server 8000`，然后打开 http://localhost:8000。

## 数据

编辑 spots.json 可修改价格和销售状态。`number` 为高清原图编号；`id` 保留为内部稳定标识。所有报价和销售状态均为模拟数据。

编号核对：H 区 328 个（原图 H079 后为 H082，保留跳号），I 区 195 个，J 区 42 个（J196–J237）。合并原先被拆成两个点击区域的 H058、I-015、H228，共 565 个独立车位。子母车位按图中一个编号计一个可选单元。

底图 `plan-hd.webp` 为 4962 × 3509 像素；交互坐标沿用 1536 × 1086 的逻辑坐标。

所有页面资源使用相对路径，可部署在 GitHub Pages 项目子路径。无需 API key 或后端服务。

第三方组件：Leaflet 1.9.4（BSD-2-Clause）。
