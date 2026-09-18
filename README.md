# 知途学习资料客服问答

这是一个基于 Langflow、Ollama 和 Chroma Local 构建的本地知识库客服问答项目。系统使用本地模型检索学习资料，并通过 RAG 流程回答电商客服问题；当知识库没有相关信息时，会拒绝猜测并提示转人工。

## 项目特点

- 本地运行，不需要付费 API 密钥
- 使用 `nomic-embed-text:latest` 生成向量
- 使用 `qwen2.5:0.5b` 生成中文回答
- 使用 Chroma Local 保存向量数据
- 仅用于学习和功能演示，不连接真实订单或支付系统

## 目录

- `knowledge/study-materials-faq.md`：演示用学习资料与客服 FAQ

## 运行前提

1. 安装 Langflow、Ollama，并启动本地 Ollama 服务。
2. 拉取模型：

   ```powershell
   ollama pull qwen2.5:0.5b
   ollama pull nomic-embed-text:latest
   ```

3. 在 Langflow 中配置 Ollama 地址：`http://localhost:11434`。
4. 创建知识库并上传 `knowledge/study-materials-faq.md`，选择 `nomic-embed-text:latest`。
5. 使用本地 `qwen2.5:0.5b` 作为语言模型运行 RAG 流程。

## 说明

知识库中的店铺、商品和政策均为虚构测试数据，不代表真实商业信息。Ollama 模型文件、虚拟环境、缓存和本地向量数据库不放入本仓库。
