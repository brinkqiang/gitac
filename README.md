# GitAutoCommit(gitac) 命令行工具

自动化生成标准Git提交说明的中英双语助手，基于代码变更分析。

## 命令行参数

### 常用选项
```bash
# 使用火山引擎配置（需设置环境变量VOLCENGINE_API_KEY）
./gitac --config_name=volcengine-deepseek-r1

# 自定义模型端点
./gitac --base_url=https://api.deepseek.com/v1 --model=deepseek-chat --api_key=<sk-xxxxxxx> --has_confirm=true

# 其他参数 --help查看
./gitac --help
```

### 火山引擎配置
1. 前往[火山引擎控制台](https://console.volcengine.com/ark/region:ark+cn-beijing/apiKey)申请API Key
2. 设置环境变量：
```bash
export VOLCENGINE_API_KEY=<YOUR_API_KEY>
```
3. 运行程序：
```bash
./gitac --config_name=volcengine-deepseek-r1
```

## 完整参数

| 参数          | 必选 | 说明                          | 示例值                      |
|---------------|------|-------------------------------|----------------------------|
| --api_key     | 否   | API认证密钥                   | sk-xxxxxxxxxxxxxxxxxxxxxx |
| --model       | 否   | 指定AI模型名称                | deepseek-chat              |
| --base_url    | 否   | 自定义API端点地址             | https://api.example.com    |
| --has_confirm   | 否   | 是否需要确认                  | true                       |
| --config_name | 否   | 使用内置配置（默认volcengine）| volcengine-deepseek-r1     |

## 输出示例

![Mobile Preview](/images/gitac_use.png)


## 使用注意事项

1. 请在Git仓库根目录执行命令
2. 确保API密钥有效且网络通畅
3. 提交前确认生成内容准确性
