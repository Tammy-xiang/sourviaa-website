SOURVIAA 网站初始版本（静态网站）

文件说明：
- index.html：主页
- products.html：产品目录
- mahjong.html：美式麻将品类页
- services.html：采购服务页
- about.html：关于我们
- contact.html：联系与询价表单
- styles.css：页面样式
- script.js：移动端导航、年份和询价表单脚本

上线前必须完成：
1. 打开 script.js，将 YOUR-EMAIL@example.com 替换成你真实接收询盘的邮箱地址。
2. 替换/确认所有产品图片与产品描述。当前麻将视觉为 CSS 制作的示意图，不是实际产品照片。
3. 确认页面上的服务描述符合你真实能够提供的服务。
4. 测试表单。当前表单会尝试打开访客自己的邮件应用，不会在网站后台保存询盘；若要可靠接收客户信息，需要后续接入表单服务或后端。
5. 检查手机端、所有导航链接和拼写。

Cloudflare Pages 部署（无需构建命令的静态站点）：
1. 将整个 sourviaa-site 文件夹中的文件上传到 GitHub 仓库（仓库根目录直接放 index.html 等文件）。
2. 登录 Cloudflare Dashboard，进入 Workers & Pages / Pages，创建 Pages 项目并连接 Git 仓库。
3. 对纯静态 HTML 网站，Build command 留空，Build output directory 填 / 或按当前界面要求选择仓库根目录。
4. 部署成功后先使用 Cloudflare 提供的 *.pages.dev 地址测试。
5. 在 Pages 项目的 Custom domains 中添加 sourviaa.com 和 www.sourviaa.com，按照 Cloudflare 提示完成域名配置。
6. 不要随意删除已有 DNS 记录，尤其是已用于邮箱的 MX、SPF、DKIM 等记录。

注意：域名连接界面会随 Cloudflare 产品更新而变化，请以当前 Dashboard 的提示为准。建议先部署测试域名，确认页面正常后再绑定正式域名。
