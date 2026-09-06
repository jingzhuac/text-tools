# 部署为无头工具站（免后端，全静态）

本工具是一个纯静态单页，**不需要任何服务器/数据库**。把它作为站点根目录的 `index.html` 部署即可。

## 推荐：GitHub Pages（免费、可长线、可自定义域名）

需要：一个 GitHub 账号（**必须由项目负责人亲自建立/授权**，见下方“红线”）。

```bash
# 1) 在本项目目录初始化发布仓库（示例公开名 text-tools）
cd projects/text-tools
git init -b main
git add .
git commit -m "release v1"

# 2) 关联远端（把 <USER> 换成你的 GitHub 用户名）
git remote add origin https://github.com/<USER>/text-tools.git
git push -u origin main
```

3. 到 GitHub 仓库 → **Settings → Pages** → Source 选 `main` / 根目录 → 保存。
4. 数秒后可访问：`https://<USER>.github.io/text-tools/`
5. （可选）绑定自有域名：仓库加 `CNAME` 文件 + DNS 解析。

> 记得提交 `.nojekyll`（本目录已包含），避免 Jekyll 干扰纯静态页。

## 备选：Netlify Drop（最快，先验证有没有人来）
- 打开 https://app.netlify.com/drop
- 直接把**本目录里的 `index.html`** 拖进去
- 即得 `https://<随机>.netlify.app` 的公开临时链接——很适合先验证“公开后有没有真实访问”。

## 备选：Vercel / Cloudflare Pages
均支持免服务器部署、免费额度充足；CLI：`vercel` / `wrangler pages deploy`，同样需账号登录。

---

## ⚠️ 红线（务必先读）
- **创建/使用账号属于“代表身份注册”**，涉及负责人身份与公开暴露，**必须由负责人（董事长）本人拍板并参与**，助理不得代办或使用聊天凭据。
- 默认仓库公开即代表**工具与内容会公开展示于网络**；推送前请确认无敏感信息。
- 推送 GitHub 属于**对外发布**，需负责人明确批准后才执行。
