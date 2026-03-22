# MiroFish Docker 部署指南

> 📌 本案例使用 **MiniMax API** 演示，支持任意 OpenAI-Compatible 模型（OpenAI、Anthropic、Groq、硅基流动、Ollama 等）。

## 🚀 快速部署

```bash
git clone https://github.com/666ghj/MiroFish.git ~/workspace/MiroFish
cd ~/workspace/MiroFish
cp .env.example .env
# 编辑 .env 填入你的 API Key
docker run -d --name mirofish \
  --env-file .env \
  -e HTTP_PROXY="" -e UV_NO_PROXY=1 \
  -p 3000:3000 -p 5001:5001 \
  ghcr.nju.edu.cn/666ghj/mirofish:latest
```

详细步骤见 [DOCKER_DEPLOY.md](./DOCKER_DEPLOY.md)

## 📖 文档内容

- 完整部署步骤（7 步）
- 前置条件检查
- 多模型支持说明
- 常见问题与解决
- 常用 Docker 命令
- 本地构建备选方案
