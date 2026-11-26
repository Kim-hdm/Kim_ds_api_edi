DeepSeek 对话客户端（自备 API Key）
一个纯前端、数据留在本机的 DeepSeek 对话界面。使用你自己的 DeepSeek 官方付费 API Key，不受网页版/App 免费额度限制。API Key 仅存于浏览器 localStorage，源码不内置任何密钥。

⚠️ 状态说明：GitHub Gist 云同步机制目前尚未完善，可能存在同步失败、冲突或数据覆盖风险。欢迎提交 PR 共同改进。

特性
自备 Key，绕开免费限制：填入 DeepSeek 官方 API Key（付费） 即可使用，不受免费版使用上限约束。
纯本机存储：API Key、对话历史均保存在浏览器本地，不上传至任何第三方服务器。
对话分支树：支持从对话节点分叉，形成可展开/折叠、可缩放平移的分支树视图，方便对比不同对话方向。
联网搜索：可选开启 DeepSeek 服务端 deepseek_web_search 工具（需选用 deepseek-flash 并连接官方接口，第三方网关可能不支持）。
图片与文本文件上传：图片本地压缩后以 OpenAI 视觉格式发送；支持 txt / md / json / 代码等文本类文件随消息发送（二进制文件暂不支持）。
智能标题整理：首句后生成临时标题，首答完成后结合问答生成陈述式短标题；支持手动重命名后不再自动改写。
接口地址可替换：默认官方地址，也可填入兼容 OpenAI 格式的第三方网关。
快速开始
打开页面：https://kim-hdm.github.io/Kim_ds_api_edi/
点击「API 设置」，填入你的 DeepSeek API Key。
如需云同步，可同时填入 GitHub Token（Classic ghp_ 或 Fine-grained github_pat_，细粒度需授予 Gist 读写权限）。
保存后即可开始对话。
需要最新信息时，点开「联网搜索」并选择 deepseek-flash 模型。
API Key 仅保存在本机浏览器 localStorage，不会上传到其他服务器。

云同步（GitHub 私有 Gist）
支持 Classic 与 Fine-grained Token；Fine-grained 需授予 Gists → Read and write 权限。
Gist ID 留空时，首次保存会自动新建一个私有 Gist；填写同一 Gist ID 可在多台设备间共享历史。

欢迎提交 Issue 和 PR。当前最需要帮助的方向包括：

PDF
