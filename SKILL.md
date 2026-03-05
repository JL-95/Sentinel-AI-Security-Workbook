# Network Proxy Skill / 联网代理规则

## Rule (Mandatory)
All network operations MUST go through the local proxy:
- Proxy URL: `http://127.0.0.1:2080`

所有联网操作必须走本地代理：
- 代理地址：`http://127.0.0.1:2080`

## Scope
This applies to all outbound traffic, including but not limited to:
- `git clone / fetch / pull / push`
- Package managers (`pip`, `npm`, `yarn`, `pnpm`, etc.)
- API calls (`curl`, SDK requests)
- Any script/tool that needs internet access

本规则适用于所有外网请求，包括但不限于：
- `git clone / fetch / pull / push`
- 包管理器（`pip`、`npm`、`yarn`、`pnpm` 等）
- API 请求（`curl`、各类 SDK）
- 任何需要联网的脚本或工具

## Git Configuration (Repo-level)
```bash
git config http.proxy http://127.0.0.1:2080
git config https.proxy http://127.0.0.1:2080
```

## Verification
```bash
git config --get http.proxy
git config --get https.proxy
```
Expected output should be:
- `http://127.0.0.1:2080`

预期输出应为：
- `http://127.0.0.1:2080`
