# 注意，现在不建议使用了，可能会被deno封号，慎用！！！
注意，现在不建议使用了，可能会被deno封号，慎用！！！

# cfll-gemini

自己用的 gemini 反向代理服务，基于免费且强大的 [Deno Deploy](https://deno.com/deploy) 平台。

## 你是否遇到过这种情况？

> *   在服务器上部署了心爱的 gemini
却提示不在可提供使用的地区或是直接就打不开网页


## 解决方案：gemini ✨

本项目 `cfll-gemini` 提供了一个简单、免费且有效的解决方案：

利用 Deno Deploy 的全球边缘网络为你创建一个专属的 gemini 资源代理。只需简单几步部署。

## 主要特性

*   🚀 **加速访问**: 通过 Deno Deploy 全球节点代理 gemini 请求，有效解决网络问题。
*   🆓 **免费部署**: 利用 Deno Deploy 的慷慨免费套餐，零成本搭建和运行。
*   🔧 **一键部署**: 提供 Deno Deploy 按钮，简化部署流程。
*   🔒 **专属服务**: 你将拥有一个自己控制的、独立的代理服务地址。

## 部署与使用教程

按照以下步骤，轻松部署你自己的 gemini 代理服务：

1.  **(可选但推荐)** 给本项目点个 [**Star ⭐**]，你的支持是作者更新和维护的动力！
2.  **Fork 本项目**: 点击页面右上角的 [**Fork**]， 按钮，将此项目复刻到你自己的 GitHub 账号下。
3.  **登录 Deno Deploy**: 访问 [Deno Deploy](https://dash.deno.com/) 并使用你的 GitHub 账号登录（如果尚未注册，会自动引导注册）。
4.  **创建新项目**:
    *   点击 **New Project** (或 **新建项目**)。
    *   选择 **Deploy from GitHub repository** (带有 GitHub 图标的那个选项)。
    *   授权 Deno Deploy 访问你的 GitHub 仓库。
5.  **选择仓库**: 在仓库列表中，找到并选择你刚刚 Fork 的 `cfll-gemini` 项目。
6.  **配置部署**:
    *   **Production Branch**: 保持默认 (`main`) 即可。
    *   **Entrypoint**: **这是关键步骤！** 点击下拉框，找到并选择 `deno_index.ts` 文件作为入口点。
    *   **Project Name**: Deno 会自动生成一个项目名称，这将是你的服务地址的一部分。你可以保留自动生成的名称 (例如 `DragonEmpery-gemini-12`)，也可以自定义一个**全局唯一**的名称 (例如 `my-gemini`)。 记下这个名称，你的服务最终地址将是 `https://<你的项目名>.deno.dev`。
7.  **开始部署**: 确认设置无误后，点击 **Link** 或 **Deploy** 按钮。Deno 将自动拉取代码、构建并部署你的服务。稍等片刻即可完成。
8.  **获取服务地址**: 部署成功后，页面会显示你的服务地址，格式为 `https://<第6步设置的项目名>.deno.dev`。复制这个地址。
9.  **配置 gemini的api**:
    *   回到你的 api接口代码中。
    *   将https://generativelanguage.googleapis.com/ 修改为 https://<第6步设置的项目名>.deno.dev。
    *   保存并退出

🎉 **完成！** 现在 gemini，将会通过你刚刚部署的 Deno 服务进行代理访问。

## 验证部署

部署完成后，你可以通过直接在浏览器中访问你的 Deno 服务地址来验证是否成功：
`https://<你的项目名>.deno.dev`
网页会显示：这个地址仅用于访问Gemini API使用！


## 注意事项

*   **魔改 AstrBot中github免费加速项目设计**: 本项目主要解决了 gemini 在国内网络环境，或被gemini封禁国外ip时可能遇到的网络问题。并非一个通用的 gemini 网站或 API 代理。
*   **Deno Deploy 免费额度**: Deno Deploy 提供非常慷慨的免费套餐（包括每月大量的请求数和数据传输量），对于 gemini 的使用场景通常绰绰有余。但仍需注意，超出免费额度可能会产生费用或服务受限，请自行查阅 [Deno Deploy Pricing](https://deno.com/deploy/pricing)。
*   **更新**: 如果本项目有重要更新，你可能需要同步你 Fork 的仓库，Deno Deploy 通常会自动重新部署更新后的代码。

---

希望这个 `cfll-gemini` 项目能帮助你顺畅地使用 gemini ！
