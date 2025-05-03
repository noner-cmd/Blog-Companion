### 使用说明
### 此项目需要在 [https://github.com/noner-cmd/Triangle-blog](此项目) 的基础上使用
#### 一、文件目录结构要求
1. **在根目录手动创建 `DCIM` 文件夹**，用于存储即刻图片。  
2. 将 `index.php` 放置在 **`admin` 子文件夹**内。  
3. 其余 6 个 PHP 文件（除 `index.php`的其他文件）放置在 **根目录**。  


#### 二、参数修改说明
1. **入口密码设置**  
   - 打开 `admin/index.php`，修改 `password` 值（默认值：`admin`）。  

2. **音乐功能配置（`music.php`）**  
   - **歌单 ID**：从分享链接中提取（例如：`https://music.163.com/m/playlist?id=3236900000&creatorId=2142752671` 中的 `2142752671`）。  
   - **Token 申请**：前往 [https://www.alapi.cn/api/14/introduction](https://www.alapi.cn/api/14/introduction) 免费申请（每日 100 次额度，每次刷新消耗 2 次）。  
   - **自动更新**：运行 `music.php` 后，`music.json` 会自动刷新，首页“最近在听”板块同步更新。  


#### 三、重要提示
1. **更新性质**：本次更新为非必要更新，主要功能为便捷操作 JSON。  
2. **安全风险**：所有 PHP 文件未进行复杂安全保护，安全性未知，建议谨慎用于生产环境。  


#### 四、文件结构示例
```
根目录/
├─ DCIM/               # 图片存储文件夹（需手动创建）
├─ admin/              # 管理文件夹
│  └─ index.php        # 登录入口文件
├─ music.php           # 音乐功能文件（根目录）
├─ ...（其余5个PHP文件）
```
