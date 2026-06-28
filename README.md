# 古伦木器·寻根完整网站

Next.js App Router + TypeScript + Tailwind CSS 的工程化版本，主导航沿用原 HTML 体系：

- 首页
- 文化溯源
- 非遗长河
- AI融合生图
- 知识库
- 我的

## 安装依赖

```bash
npm install
```

当前项目包含 Prisma 预留 schema，但页面与 API 默认使用 mock store。为避免 Windows `cmd.exe` 在中文路径下执行 Prisma preinstall 脚本出现 `Access is denied`，项目 `.npmrc` 已设置 `ignore-scripts=true`。

## 本地启动

```bash
npm run dev
```

默认脚本已使用 `--hostname 0.0.0.0`，同一局域网内其他设备可通过你的电脑局域网 IP 访问。

## 构建

```bash
npm run build
```

## AI 接入预留

复制 `.env.example` 为 `.env`，后续按实际供应商填写：

```env
AI_PROVIDER="mock"
AI_API_KEY=""
AI_BASE_URL=""
AI_MODEL=""
```

当前默认使用 Mock Provider，页面调用路径已经是 API Route，后续替换 Provider 即可接真实服务。

## 数据库预留

已提供 Prisma schema，默认 SQLite：

```bash
npm run prisma:generate
npm run prisma:migrate
```

当前 API 使用内存 mock store，后续可把 `lib/server/mock-store.ts` 替换为 Prisma 查询。
