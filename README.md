# Mansong Limited — Official Website

漫松有限公司官方网站（中英双语） / Official bilingual (Chinese / English) website of Mansong Limited.

- 线上地址 / Live URL: https://mansong.hk
- 托管方式 / Hosting: GitHub Pages（仓库根目录静态站点，含 `CNAME` 自定义域名文件）

## 本地预览 / Local Preview

直接用浏览器打开 `index.html` 即可，无需构建步骤。

Open `index.html` in any browser — no build step required.

## 站点结构 / Structure

```
index.html      单页站点（含中英文切换，右上角 EN/中文 按钮）
assets/logo.jpg 公司 Logo（取自产品手册封面）
CNAME           GitHub Pages 自定义域名 mansong.hk
.nojekyll       跳过 Jekyll 处理，静态原样发布
```

## 修改语言内容 / Editing Languages

页面中所有文案均为 `<span class="zh">中文</span><span class="en">English</span>` 成对结构，
直接编辑对应 span 即可；语言偏好保存在浏览器 localStorage（键 `ms-lang`）。

All copy is stored in paired `<span class="zh">…</span><span class="en">…</span>` elements.
Edit in place; the visitor's language preference is persisted in localStorage (`ms-lang`).

## 待补充信息 / TODO

- [ ] 核实联系电话（目前为手册占位号码 +852 1234 5678）
- [ ] 核实商务邮箱（info@mansonglimited.com）与 mansong.hk 域名邮箱的对应关系
- [ ] 替换为正式的 WhatsApp / 微信二维码（如需要）

## 域名解析 / DNS（mansong.hk → GitHub Pages）

在域名注册商处添加：

| 类型 | 主机记录 | 记录值 |
| --- | --- | --- |
| A | @ | 185.199.108.153 |
| A | @ | 185.199.109.153 |
| A | @ | 185.199.110.153 |
| A | @ | 185.199.111.153 |
| CNAME | www | tangym208.github.io |

DNS 生效后，在 GitHub 仓库 Settings → Pages 中确认自定义域为 `mansong.hk`，
并勾选 **Enforce HTTPS**（证书自动签发，需等待 DNS 校验通过）。
