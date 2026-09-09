---
theme: default
title: AI Coding：从原理到实践
aspectRatio: 16/9
canvasWidth: 1280
transition: fade
mdc: true
fonts:
  sans: "PingFang SC,Hiragino Sans GB,Microsoft YaHei,Arial,sans-serif"
  mono: "SFMono-Regular,Menlo,Monaco,Consolas,Liberation Mono,monospace"
  provider: none
---

<div class="editorial-slide cover">
  <div class="cover-left">
    <h1><span class="cover-title-en">AI Coding</span><span class="cover-title-cn">从原理到实践</span></h1>
    <div class="cover-rule"></div>
    <p class="cover-subtitle">从模型趋势与 Agent 原理出发，认识 Coding Agent 工具链，<br />了解工作流与工程实践。</p>
  </div>
  <div class="cover-right">
      <img class="cover-agent-illustration" src="/images/cover-agent-orchestration-transparent.png" alt="AI Coding Agent 编排文档、终端、浏览器与工具的工作流插画" aria-hidden="true" />
  </div>
</div>

---

<div class="editorial-slide toc">
  <h1 class="title">内容概览</h1>
  <div class="toc-list">
    <div class="toc-row"><strong>一</strong><h3>AI Coding 的发展与趋势</h3></div>
    <div class="toc-row"><strong>二</strong><h3>Agent 基本原理</h3></div>
    <div class="toc-row"><strong>三</strong><h3>AI Coding 工具链</h3></div>
    <div class="toc-row"><strong>四</strong><h3>AI Coding 工作流</h3></div>
    <div class="toc-row"><strong>五</strong><h3>思考</h3></div>
  </div>
</div>

---

<div class="editorial-slide chapter-page">
  <div class="chapter-index">第一章</div>
  <div class="chapter-copy">
    <h1>AI Coding 的发展与趋势</h1>
  </div>
</div>

---

<div class="editorial-slide evolution-page">
  <h1 class="title">AI Coding 的发展</h1>
  <div class="evolution-track" aria-hidden="true"></div>
  <div class="evolution-stages">
    <article class="evolution-stage stage-completion">
      <div class="stage-heading"><strong>1.0</strong><span>2021—2022 年底</span></div>
      <h3>代码补全</h3>
      <div class="stage-detail"><b>代表工具</b><p>GitHub Copilot（初代插件）、Tabnine</p></div>
      <div class="stage-detail"><b>协作方式</b><p>AI 行内预测代码，开发者按 Tab 采纳。</p></div>
    </article>
    <article class="evolution-stage stage-assistant">
      <div class="stage-heading"><strong>2.0</strong><span>2023—2024 年底</span></div>
      <h3>编程助手</h3>
      <div class="stage-detail"><b>代表工具</b><p>GitHub Copilot Chat、早期 Cursor、早期 Cline</p></div>
      <div class="stage-detail"><b>协作方式</b><p>AI 能理解项目，并同时修改多个相关文件。开发者负责检查和确认结果。</p></div>
    </article>
    <article class="evolution-stage stage-agent">
      <div class="stage-heading"><strong>3.0</strong><span>2025—至今</span></div>
      <h3>Agent</h3>
      <div class="stage-detail"><b>代表工具</b><p>Claude Code、Cursor、Codex</p></div>
      <div class="stage-detail"><b>协作方式</b><p>开发者给出目标，Agent 自主执行、测试和修复。</p></div>
      <div class="stage-detail"><b>产品形态</b><p>CLI、IDE、Workbench 是三种产品形态，不代表能力等级。</p></div>
    </article>
  </div>
</div>

---

<div class="editorial-slide multi-agent-page">
  <h1 class="title">Cloud Agent 与 Multi-Agent</h1>
  <div class="multi-agent-layout">
    <div class="multi-agent-content">
      <div class="agent-parallel-grid">
        <section class="agent-lane cloud-lane">
          <div class="track-heading"><h2>Cloud Agent</h2><span>代表产品</span></div>
          <p>Agent 从本地走向云端，在独立环境中执行长任务；开发者从实时协作转向目标管理。</p>
          <div class="parallel-products">
            <div class="parallel-product"><strong>Codex Cloud</strong><p>云端独立环境，支持异步执行与长任务。</p></div>
            <div class="parallel-product"><strong>Cursor Cloud Agents</strong><p>把本地编辑转向云端任务执行。</p></div>
            <div class="parallel-product"><strong>GitHub Copilot cloud agent</strong><p>由 Issue 驱动执行，并回到 PR 协作。</p></div>
          </div>
        </section>
        <section class="agent-lane multi-lane">
          <div class="track-heading"><h2>Multi-Agent</h2><span>代表产品</span></div>
          <p>多个不同品牌或不同角色的 Agent 并行执行、分工协作、统一编排。</p>
          <div class="parallel-products">
            <div class="parallel-product"><strong>Grok Bot</strong><p>持久化 Bot 组成团队，支持云端并行与任务交接。</p></div>
            <div class="parallel-product"><strong>Multica</strong><p>接入不同品牌 Agent，统一分派与运行监控。</p></div>
            <div class="parallel-product"><strong>Raft</strong><p>连接 Human 与 Agent，支持并行工作与人工 Review。</p></div>
          </div>
        </section>
      </div>
    </div>
    <div class="multi-agent-art"><img src="/images/multi-agent-cloud-robots-transparent.png" alt="多个 Agent 在云上并行协作" /></div>
  </div>
  <div class="next-trend"><strong>趋势</strong><p>Agent 正变得更自主、运行时间更长，并逐步走向云端异步执行与多 Agent 协作。</p></div>
</div>

---

<div class="editorial-slide model-page model-chart-page">
  <h1 class="title">模型发展趋势</h1>
  <div class="model-full-image"><img src="/images/image-1.png" alt="模型发展时间线" /></div>
</div>

---

<div class="editorial-slide model-tier-page">
  <h1 class="title">主流模型</h1>
  <div class="model-tier-list">
    <section class="model-tier-row tier-frontier">
      <div class="model-tier-label"><strong>1</strong><div><h2>顶级模型</h2><span>能力上限</span></div></div>
      <div class="model-tier-models">
        <span>GPT-6 Astra</span><span>Claude Fable 5.1</span><span>Claude Fable 5</span>
        <span>Claude Opus 5</span><span>GPT-5.6 Sol</span>
      </div>
    </section>
    <section class="model-tier-row tier-frontline">
      <div class="model-tier-label"><strong>2</strong><div><h2>强模型</h2><span>综合能力</span></div></div>
      <div class="model-tier-models">
        <span>Kimi K3</span><span>GLM-5.3</span><span>Qwen3.8 Max</span>
        <span>Grok 4.6</span><span><s>DeepSeek V4 Pro</s></span>
      </div>
    </section>
    <section class="model-tier-row tier-efficient">
      <div class="model-tier-label"><strong>3</strong><div><h2>高效模型</h2><span>速度与成本</span></div></div>
      <div class="model-tier-models">
        <span>Gemini 3.8 Flash</span><span>GLM-5.3-Flash</span><span>GPT-5.6 Luna</span>
        <span>Qwen3.8-Flash-Next</span><span>DeepSeek V4 Flash</span>
      </div>
    </section>
  </div>
</div>

---

<div class="editorial-slide model-trends-page">
  <h1 class="title">模型趋势解读</h1>
  <ul class="bullet-list trend-grid">
    <li><div class="trend-item-copy"><div class="trend-main"><strong>Agent 化：</strong><span>从单轮回答走向长时间、多步骤任务执行，能够规划、调用工具、验证并持续完成。</span></div><div class="trend-meta">代表：GPT-6 Astra、Claude Fable 5.1</div></div></li>
    <li><div class="trend-item-copy"><div class="trend-main"><strong>能力与效率并行：</strong><span>旗舰模型持续冲击能力上限，轻量模型则追求更低延迟、更低成本和更高并发。</span></div><div class="trend-meta">效率路线：GPT-5.6 Luna、DeepSeek-V4-Flash</div></div></li>
    <li><div class="trend-item-copy"><div class="trend-main"><strong>环境交互原生化：</strong><span>模型开始针对浏览器、桌面和专业软件环境专项训练，从“理解信息、调用 API”走向“理解界面、直接操作并完成任务”。</span></div><div class="trend-meta">代表：GPT-6 Astra 的 Computer Use</div></div></li>
    <li><div class="trend-item-copy"><div class="trend-main"><strong>模型与 Harness 协同演进：</strong><span>模型提升能力上限，Harness 从“弥补模型缺陷”逐步转向“组织和放大模型能力”。</span></div><div class="trend-meta">模型原生能力增强后，Prompt、Skill 和规则会逐步去除历史补丁</div></div></li>
    <li><div class="trend-item-copy"><div class="trend-main"><strong>递归自我改进（RSI）：</strong><span>前沿模型已经开始参与下一代模型的研发与改进，推动模型研发与迭代加速。</span></div></div></li>
  </ul>
</div>

---

<div class="editorial-slide chapter-page">
  <div class="chapter-index">第二章</div>
  <div class="chapter-copy">
    <h1>Agent 基本原理</h1>
  </div>
</div>

---

<div class="editorial-slide agent-concept-page">
  <h1 class="title">Agent 的基本概念</h1>
  <div class="agent-focus-layout">
    <section class="agent-equation-panel">
      <div class="agent-equation-block">
        <div class="agent-equation-main">Agent = Model + Harness</div>
      </div>
      <div class="agent-equation-divider"></div>
      <div class="agent-equation-block coding-equation-block">
        <div class="agent-equation-label">Coding Agent</div>
        <p>面向 SWE（Software Engineering）场景的 Agent，通常具备文件读写、代码搜索、Shell、测试、Git 等工具。</p>
      </div>
    </section>
    <section class="agent-harness-panel">
      <h2>Harness</h2>
      <div class="agent-harness-identity">模型之外的运行框架</div>
      <div class="agent-harness-formula">上下文管理 + 工具接口<br />+ 约束 + 验证 + 纠正</div>
    </section>
  </div>
  <div class="agent-extension-note">通用 Agent 可进一步扩展 Web、Browser、Apps 等能力，而 Coding 正逐渐成为其重要的通用执行能力。</div>
</div>

---

<div class="editorial-slide agent-loop-page">
  <h1 class="title">Agent Loop</h1>
  <div class="loop-layout">
    <div class="loop-animation" role="img" aria-label="Agent Loop 从消息进入模型，经工具判断与执行后，把结果写回消息列表的循环动画">
      <div class="agent-loop-diagram">
        <div class="loop-flow-node loop-user-node">
          <strong>用户提问</strong>
          <span>“帮我创建 hello.py”</span>
        </div>
        <div class="loop-flow-node loop-messages-node">
          <strong>messages[]</strong>
          <span>累积式消息列表</span>
        </div>
        <div class="loop-flow-node loop-model-node">
          <strong>大模型（LLM）</strong>
          <span>模型阅读消息历史</span>
          <span>判断：需要工具吗？</span>
          <span>返回 finish_reason 信号</span>
        </div>
        <div class="loop-decision-node">
          <div class="loop-decision-content"><strong>finish_reason</strong><span>== “tool_calls”？</span></div>
        </div>
        <div class="loop-flow-node loop-result-node">
          <strong>返回结果</strong>
          <span>循环结束</span>
        </div>
        <div class="loop-flow-node loop-tool-node">
          <strong>执行工具调用</strong>
          <span>Edit(path, content)</span>
        </div>
        <svg class="loop-flow-svg" viewBox="0 0 1000 600" preserveAspectRatio="none" aria-hidden="true">
          <defs>
    <marker id="loop-arrow-head" viewBox="0 0 10 10" refX="9" refY="5" markerWidth="4.5" markerHeight="4.5" orient="auto-start-reverse">
              <path d="M 0 0 L 10 5 L 0 10 z" fill="#16150f" />
            </marker>
          </defs>
          <g class="loop-svg-base">
            <path d="M 220 123 L 220 162" />
            <path d="M 390 216 L 500 216" />
            <path d="M 720 222 L 720 244 L 645 244 L 645 264" />
            <path d="M 790 338 L 805 338 L 805 366 L 820 366" />
            <path d="M 645 412 L 645 438 L 720 438 L 720 462" />
            <path d="M 500 516 L 40 516 L 40 216 L 50 216" />
          </g>
          <g class="loop-svg-motion">
            <path d="M 220 123 L 220 162" />
            <path d="M 390 216 L 500 216" />
            <path d="M 720 222 L 720 244 L 645 244 L 645 264" />
            <path d="M 790 338 L 805 338 L 805 366 L 820 366" />
            <path d="M 645 412 L 645 438 L 720 438 L 720 462" />
            <path d="M 500 516 L 40 516 L 40 216 L 50 216" />
          </g>
        </svg>
        <div class="loop-feedback-label">追加 tool_result 到 messages</div>
        <span class="loop-branch-label loop-no-label">否</span>
        <span class="loop-branch-label loop-yes-label">是</span>
      </div>
    </div>
    <div class="loop-react-copy">
      <p><strong>一次任务，多轮请求</strong><br />Model 返回 Tool Call 时，Agent 执行 Tool，并把 Tool Result 写回 Messages。下一轮请求读取更新后的 Context，继续决定下一步。只有 Model 直接返回最终结果，或触发停止条件，Loop 才结束。</p>
    </div>
  </div>
</div>

---

<div class="editorial-slide loop-request-page">
  <h1 class="title">Agent Loop：第一次请求</h1>
  <div class="loop-json-grid">
    <section class="loop-json-panel loop-json-request">
      <h2>发给模型</h2>
      <pre class="loop-json-code"><code>{
  "model": <span class="json-blue">"glm-5.2"</span>,
  "messages": [
    { "role": <span class="json-yellow">"user"</span>, "content": "创建 hello.py，打印 Hello, World!" }
  ],
  "tools": [{
    "type": "function",
    "function": {
      "name": <span class="json-pink">"Edit"</span>,
      "parameters": {
        "type": "object",
        "required": ["path", "content"]
      }
    }
  }]
}</code></pre>
    </section>
    <section class="loop-json-panel loop-json-response">
      <h2>模型返回</h2>
      <pre class="loop-json-code"><code>{
  "model": <span class="json-blue">"glm-5.2"</span>,
  "choices": [{
    "finish_reason": <span class="json-pink">"tool_calls"</span>,
    "message": {
      "role": "assistant",
      "content": null,
      "tool_calls": [{
        "id": "call_abc123",
        "type": "function",
        "function": {
          "name": <span class="json-pink">"Edit"</span>,
          "arguments": "{\"path\":\"hello.py\",\"content\":\"print('Hello, World!')\"}"
        }
      }]
    }
  }]
}</code></pre>
    </section>
  </div>
  <div class="loop-request-caption"><strong>第一次请求</strong><span>模型没有直接回答，而是返回 <code>tool_calls</code>，要求 Harness 执行 <code>Edit</code>。</span></div>
</div>

---

<div class="editorial-slide loop-request-page loop-second-request-page">
  <h1 class="title">Agent Loop：第二次请求</h1>
  <div class="loop-json-grid">
    <section class="loop-json-panel loop-json-request">
      <h2>再次发给模型</h2>
      <pre class="loop-json-code"><code>{
  "model": <span class="json-blue">"glm-5.2"</span>,
  "messages": [
    { "role": "user", "content": "创建 hello.py，打印 Hello, World!" },
    { "role": "assistant", "content": null,
      "tool_calls": [{
        "id": "call_abc123",
        "type": "function",
        "function": { "name": <span class="json-pink">"Edit"</span>,
          "arguments": "{\"path\":\"hello.py\",\"content\":\"print('Hello, World!')\"}"
        }}
      ]},
    { "role": <span class="json-yellow">"tool"</span>, "tool_call_id": "call_abc123",
      "content": "{\"success\":true,\"path\":\"hello.py\"}" }
  ],
  "tools": [{
    "type": "function",
    "function": { "name": <span class="json-pink">"Edit"</span>,
      "parameters": { "type": "object", "required": ["path", "content"] }
  }}]
}</code></pre>
    </section>
    <section class="loop-json-panel loop-json-response">
      <h2>模型最终返回</h2>
      <pre class="loop-json-code"><code>{
  "model": <span class="json-blue">"glm-5.2"</span>,
  "choices": [{
    "finish_reason": <span class="json-yellow">"stop"</span>,
    "message": {
      "role": "assistant",
      "content": "已创建 hello.py，文件内容为：\nprint('Hello, World!')"
    }
  }]
}</code></pre>
    </section>
  </div>
  <div class="loop-request-caption"><strong>第二次请求</strong><span>Harness 把工具结果作为 <code>role: tool</code> 追加到消息列表，模型读取结果后返回最终回答。</span></div>
</div>

---

<div class="editorial-slide agent-system-page">
  <h1 class="title">Agent 核心构成</h1>
  <div class="agent-architecture-visual">
    <div class="agent-architecture-stage">
      <img class="agent-architecture-image" src="/images/agent-architecture-v3.png" alt="Agent Loop 与外围 Harness 能力模块的关系图" />
      <div class="agent-architecture-note note-context"><span>组织当前任务所需的上下文信息</span></div>
      <div class="agent-architecture-note note-state"><span>维护任务进度与会话状态</span></div>
      <div class="agent-architecture-note note-tools"><span>连接并调用外部能力</span></div>
      <div class="agent-architecture-note note-execution"><span>提供实际操作与执行空间</span></div>
      <div class="agent-architecture-note note-guardrails"><span>控制权限、边界与安全约束</span></div>
    </div>
  </div>
</div>

---

<div class="editorial-slide mcp-rebuilt-page">
  <h1 class="title">MCP</h1>
  <div class="mcp-rebuilt-layout">
    <div class="mcp-rebuilt-visual"><img src="/images/mcp-architecture-v4.png" alt="Agent 直接调用内置工具，并通过 MCP 调用外部工具" /></div>
    <div class="mcp-rebuilt-copy">
      <div class="mcp-definition"><strong>MCP</strong><p>一种开放协议，让外部能力以工具的形式被 Agent 发现和调用。</p></div>
      <div class="mcp-deploy mcp-local"><h3>本地 MCP</h3><p>运行在本机，通过本地进程与 Agent 通信。</p></div>
      <div class="mcp-deploy mcp-remote"><h3>远程 MCP</h3><p>运行在服务器，通过网络与 Agent 通信。</p></div>
    </div>
  </div>
</div>

---

<div class="editorial-slide skill-rebuilt-page">
  <h1 class="title">Skills</h1>
  <p class="lead">Skill 把一类任务的方法封装成 Agent 可复用的能力单元。</p>
  <div class="skill-rebuilt-layout">
    <div class="skill-rebuilt-visual">
      <img src="/images/skill-workflow-v4.png" alt="Skill 从发现、加载、按需读取到执行的四步流程" />
    </div>
    <div class="skill-feature-note">
      <h3>五个特征</h3>
      <div class="skill-feature-list">
        <div class="skill-feature-item"><strong>可复用与可分发</strong><span>一份 Skill 可以安装、共享，并跨任务复用。</span></div>
        <div class="skill-feature-item"><strong>渐进式披露</strong><span>先发现，后加载，按需读取。</span></div>
        <div class="skill-feature-item"><strong>模块化与可组合</strong><span>小 Skill 可以组合成更复杂的能力。</span></div>
        <div class="skill-feature-item"><strong>经验可执行化</strong><span>把 SOP 和工具用法沉淀成方法。</span></div>
        <div class="skill-feature-item"><strong>可迭代与可评测</strong><span>可以独立升级和验证，无需重新训练模型。</span></div>
      </div>
    </div>
  </div>
</div>

---

<div class="editorial-slide context-rebuilt-page">
  <h1 class="title">Context</h1>
  <div class="context-rebuilt-layout">
    <section class="context-input-panel">
      <div class="context-request-title">上下文组成</div>
      <div class="context-request-stack">
        <article class="context-request-item context-request-instructions">
          <div class="context-request-number">1</div>
          <div class="context-request-body">
            <div class="context-request-heading"><b>Instructions</b></div>
            <p>系统指令 / 开发者指令 / 已加载的 Skill 指令</p>
          </div>
        </article>
        <article class="context-request-item context-request-messages">
          <div class="context-request-number">2</div>
          <div class="context-request-body">
            <div class="context-request-heading"><b>Messages</b></div>
          <p>用户输入、模型回复与 tool_call，以及 Tool Result。</p>
          </div>
        </article>
        <article class="context-request-item context-request-tools">
          <div class="context-request-number">3</div>
          <div class="context-request-body">
            <div class="context-request-heading"><b>Tools</b></div>
            <p>当前允许模型调用的 Tools，以及 MCP 提供的 Schema</p>
          </div>
        </article>
      </div>
      <div class="context-source-note">文件、代码和终端输出需要先由 Tool 读取、检索或执行，结果才会进入这次请求。</div>
    </section>
    <section class="context-window-panel">
      <div class="context-compression-title">上下文压缩</div>
      <p class="context-window-one-line">Context Window：一次请求可容纳的 Token 上限。</p>
      <div class="context-message-compression">
        <div class="context-message-strategies">
          <strong>压缩机制</strong>
          <span><b>清理 Tool Result</b><small>终端日志、搜索结果、长代码等旧输出，做删除或截断。</small></span>
          <span><b>总结历史消息</b><small>把较早的用户消息、Agent 回复和执行过程总结成 Summary。</small></span>
          <span><b>保留近期上下文</b><small>保留最近几轮 Messages 与当前任务状态。</small></span>
        </div>
      </div>
    </section>
  </div>
</div>

---

<div class="editorial-slide cache-page kv-cache-page">
  <h1 class="title">KV Cache：单次推理中的内部缓存</h1>
  <div class="kv-cache-visual">
    <img src="/images/image-5.png" alt="KV Cache 前缀复用示意" />
  </div>
</div>

---

<div class="editorial-slide cache-page prompt-cache-page">
  <h1 class="title">Prompt Cache：跨请求复用相同前缀</h1>
  <div class="prompt-cache-layout">
    <div class="prompt-cache-visual">
      <div class="image-panel"><img src="/images/image-6.png" alt="缓存命中与输入价格示意" /></div>
      <p class="prompt-cache-caption">服务商匹配请求前缀，命中后直接复用已计算结果，减少重复计算成本。</p>
    </div>
    <section class="prompt-cache-copy">
      <div class="prompt-cache-copy-head">
        <strong>缓存关系</strong>
      </div>
      <div class="prompt-cache-common">
        <p>都复用不变前缀，减少重复计算。</p>
      </div>
      <div class="prompt-cache-levels prompt-cache-levels-redesign">
        <div class="prompt-cache-level-kv"><b>KV Cache</b><span>模型内部<br />单次推理内</span></div>
        <span class="prompt-cache-level-arrow">→</span>
        <div class="prompt-cache-level-prompt"><b>Prompt Cache</b><span>推理服务<br />多次请求间</span></div>
      </div>
      <div class="prompt-cache-section prompt-cache-relation">
        <p>Prompt Cache 命中时，可复用已计算的前缀状态（通常就是 KV Cache）。</p>
      </div>
      <div class="prompt-cache-section prompt-cache-condition">
        <strong>实践启发</strong>
        <ul class="bullet-list prompt-cache-bullets">
          <li>系统提示词和工具定义保持固定。</li>
          <li>用户输入、运行结果等动态信息追加到末尾。</li>
        </ul>
      </div>
    </section>
  </div>
</div>

---

<div class="editorial-slide chapter-page">
  <div class="chapter-index">第三章</div>
  <div class="chapter-copy">
    <h1>AI Coding 工具链</h1>
    <p>开发环境&nbsp;&nbsp;Agent 选择&nbsp;&nbsp;模型配置&nbsp;&nbsp;能力扩展</p>
  </div>
</div>

---

<div class="editorial-slide environment-page">
  <h1 class="title">本地开发环境</h1>
  <div class="environment-light-grid">
    <article class="environment-item environment-item-node"><h3><a href="https://nodejs.org/en" target="_blank" rel="noreferrer">Node.js 22+</a></h3><p>运行 JavaScript / TypeScript 工具，许多 Coding Agent、MCP Server 依赖它。</p></article>
    <article class="environment-item environment-item-python"><h3><a href="https://www.python.org/" target="_blank" rel="noreferrer">Python 3+</a></h3><p>运行自动化脚本、数据处理与 Python 工具。</p></article>
    <article class="environment-item environment-item-powershell"><h3><a href="https://github.com/PowerShell/PowerShell" target="_blank" rel="noreferrer">PowerShell 7</a></h3><p>Windows 原生 Shell，Agent 调用系统能力更直接。</p></article>
    <article class="environment-item environment-item-terminal"><h3><a href="https://github.com/microsoft/terminal" target="_blank" rel="noreferrer">Windows Terminal</a></h3><p>统一承载 PowerShell、WSL 等会话，支持多标签和分屏。</p></article>
    <article class="environment-item environment-item-git"><h3><a href="https://git-scm.com/" target="_blank" rel="noreferrer">Git</a></h3><p>Git Bash 提供类 Unix 命令行；Git 负责版本管理与代码协作。</p></article>
    <article class="environment-item environment-item-wsl"><h3><a href="https://learn.microsoft.com/en-us/windows/wsl/" target="_blank" rel="noreferrer">WSL</a> <small>可选</small></h3><p>在 Windows 中运行 Linux 用户空间，兼容 Bash 和 Linux 工具链，无需双系统。</p></article>
  </div>
</div>

<!--
参考资料（官方文档与仓库）：
- Node.js: https://nodejs.org/en
- Python: https://www.python.org/
- PowerShell: https://github.com/PowerShell/PowerShell
- Windows Terminal: https://github.com/microsoft/terminal
- Git: https://git-scm.com/
- WSL: https://learn.microsoft.com/en-us/windows/wsl/
-->

---

<div class="editorial-slide harness-page">
  <h1 class="title">主流 Agent</h1>
  <div class="harness-grid">
    <article class="harness-card harness-card-claude">
      <h2><a href="https://code.claude.com/docs/en/overview" target="_blank" rel="noreferrer">Claude Code</a><strong class="harness-card-kicker">成熟生态</strong></h2>
      <p>推出较早，产品成熟度高，围绕 <strong>Skills、Hooks、Subagent、MCP、Plugin</strong> 等形成了完整的 Agent 能力与扩展生态。整体工具链和社区沉淀都比较成熟。</p>
    </article>
    <article class="harness-card harness-card-codex">
      <h2><a href="https://github.com/openai/codex" target="_blank" rel="noreferrer">Codex</a><strong class="harness-card-kicker">一体化工作台</strong></h2>
      <p>从 CLI 延伸到 <strong>Desktop 与 Cloud</strong>，形成完整的一体化 Coding Agent 工作台；<strong>Desktop 交互体验出色，Browser Use / Computer Use 实用，本地与云端任务衔接顺畅。</strong></p>
    </article>
    <article class="harness-card harness-card-opencode">
      <h2><a href="https://github.com/anomalyco/opencode" target="_blank" rel="noreferrer">OpenCode</a><strong class="harness-card-kicker">开源通用</strong></h2>
      <p><strong>完全开源、不绑定模型厂商</strong>，可自由接入不同 Provider 和本地模型。整体配置自由度和可扩展性高，是通用型开源 Coding Agent 的代表。</p>
    </article>
    <article class="harness-card harness-card-pi">
      <h2><a href="https://github.com/earendil-works/pi" target="_blank" rel="noreferrer">Pi</a><strong class="harness-card-kicker">极简底座</strong></h2>
      <p>刻意保持极简，默认核心只有 <strong>read、write、edit、bash</strong>，不预设复杂的 Agent 工作流；同时支持 <strong>Extensions、Skills、Packages</strong>，可在轻量底座上按需扩展。</p>
    </article>
    <article class="harness-card harness-card-omp">
      <h2><a href="https://github.com/Raudbjorn/omp" target="_blank" rel="noreferrer">OMP</a><strong class="harness-card-kicker">全能增强</strong></h2>
      <p>基于 Pi 做了大量工程能力增强，内置 <strong>LSP、Browser、Debugger、Subagent</strong> 等能力，并提供 <strong>Role 与模型路由</strong>。相比 Pi 更强调高级能力开箱即用，同时保留较强的可配置性。</p>
    </article>
    <article class="harness-card harness-card-dsh">
      <h2><a href="https://github.com/deepseek-ai/deepseek-harness" target="_blank" rel="noreferrer">DSH</a><strong class="harness-card-kicker">可组合架构</strong></h2>
      <p>采用 <strong>Everything is a Plugin</strong> 的架构思路，Model、Tool、Skill、Agent Loop、Session、Sandbox、UI 等模块都可以独立替换和组合。采用 <strong>本地 Host + Web</strong> 的交互方式。</p>
    </article>
  </div>
</div>

<!--
参考资料（官方文档与仓库）：
- Claude Code: https://code.claude.com/docs/en/overview
- Codex Computer Use: https://learn.chatgpt.com/docs/computer-use?translationFallback=zh-Hans
- Codex: https://github.com/openai/codex
- OpenCode: https://github.com/anomalyco/opencode
- Pi: https://github.com/earendil-works/pi
- OMP: https://github.com/Raudbjorn/omp
- DeepSeek Harness 架构: https://github.com/deepseek-ai/deepseek-harness/blob/master/docs/architecture.md
-->

---

<div class="editorial-slide cc-switch-page">
  <h1 class="title">CC Switch：配置切换与本地代理</h1>
  <div class="cc-switch-layout">
    <section class="cc-switch-intro">
      <div class="cc-switch-label">配置切换</div>
      <h2><a href="https://github.com/Hortus-Edenensis/cc-switch" target="_blank" rel="noreferrer">CC Switch</a></h2>
      <p class="cc-switch-key">管理「用哪套配置」</p>
      <p class="cc-switch-summary">把多个 Coding Agent 的连接配置集中管理，同时提供本地代理能力。</p>
      <div class="cc-switch-config">Provider · Model · API Key · Base URL</div>
    </section>
    <section class="cc-switch-details">
      <div class="cc-switch-detail"><h3>配置管理</h3><p>集中管理多套 Provider、模型、API Key、Base URL 等配置，需要时一键切换。</p></div>
      <div class="cc-switch-detail"><h3>MCP 与 Skills</h3><p>顺带统一维护 MCP Server 和 Skills，让不同 Agent 保持一致。</p></div>
      <div class="cc-switch-detail"><h3>本地代理</h3><p>支持格式转换、热切换、故障切换和 Provider 健康监测。</p></div>
    </section>
  </div>
  <div class="cc-switch-note">CC Switch 既能切换配置，也能在本地转发请求。</div>
</div>

---

<div class="editorial-slide api-formats-page">
  <h1 class="title">常见 API 格式</h1>
  <p class="lead">不同模型和 Provider 常见的接口格式包括：</p>
  <div class="api-format-stack">
    <div class="api-format-row api-format-chat">
      <div class="api-format-index">01</div>
      <div class="api-format-name"><h2>OpenAI Chat Completions</h2><code>POST /v1/chat/completions</code></div>
      <p>经典的 <code>messages</code> 对话格式，每轮请求携带全量消息历史。</p>
    </div>
    <div class="api-format-row api-format-anthropic">
      <div class="api-format-index">02</div>
      <div class="api-format-name"><h2>Anthropic Messages</h2><code>POST /v1/messages</code></div>
      <p>Claude Code 使用的消息式接口，每轮请求携带全量消息历史，工具调用采用 Anthropic 的内容块格式。</p>
    </div>
    <div class="api-format-row api-format-responses">
      <div class="api-format-index">03</div>
      <div class="api-format-name"><h2>OpenAI Responses</h2><code>POST /v1/responses</code></div>
      <p>Codex 使用的接口格式，通过 <code>previous_response_id</code> 关联上一轮响应，支持根据需要只传递新的输入和工具结果，客户端无需每次重复发送完整历史。</p>
    </div>
  </div>
</div>

---

<div class="editorial-slide gateway-page">
  <h1 class="title">模型网关</h1>
  <div class="gateway-grid">
    <section class="gateway-card gateway-9router gateway-featured">
      <div class="gateway-featured-copy">
        <div class="gateway-card-head"><h2><a href="https://github.com/decolua/9router" target="_blank" rel="noreferrer">9Router</a></h2></div>
        <div class="gateway-feature-grid">
          <div class="gateway-feature"><strong>多 Provider 接入</strong><span>通过 OAuth、API Key 等方式接入多个 Provider，OAuth Token 自动刷新。</span></div>
          <div class="gateway-feature"><strong>模型组合与多模态</strong><span>按场景组合文本、图像、音频等模型，并设置多级 Fallback。</span></div>
          <div class="gateway-feature"><strong>请求适配</strong><span>提供统一入口，转换 OpenAI、Claude、Gemini 等请求格式。</span></div>
          <div class="gateway-feature"><strong>上下文优化</strong><span>RTK、Caveman 等。</span></div>
        </div>
      </div>
    </section>
    <section class="gateway-card gateway-others">
      <div class="gateway-card-head"><h2>其他模型网关</h2><span>简要介绍</span></div>
      <div class="gateway-others-list">
        <div class="gateway-mini gateway-cliproxy">
          <div class="gateway-card-head"><h2><a href="https://github.com/router-for-me/CLIProxyAPI" target="_blank" rel="noreferrer">CLIProxyAPI</a></h2><span>CLI 代理</span></div>
          <p>把多个 CLI 账号代理成兼容多种协议的本地 API。</p>
        </div>
        <div class="gateway-mini gateway-newapi">
          <div class="gateway-card-head"><h2><a href="https://github.com/QuantumNous/new-api" target="_blank" rel="noreferrer">New API</a></h2><span>模型聚合</span></div>
          <p>面向平台化的模型聚合、渠道管理与用量计费。</p>
        </div>
        <div class="gateway-mini gateway-sub2api">
          <div class="gateway-card-head"><h2><a href="https://github.com/Wei-Shaw/sub2api" target="_blank" rel="noreferrer">Sub2API</a></h2><span>额度分发</span></div>
          <p>偏订阅额度分发、账号池管理与并发控制。</p>
        </div>
      </div>
    </section>
  </div>
</div>

---

<div class="editorial-slide web-products-page">
  <h1 class="title">WebSearch 和 WebFetch</h1>
  <div class="web-products-stage">
    <article class="web-product-card web-product-tavily">
      <div class="web-product-copy">
        <h2><a href="https://www.tavily.com/" target="_blank" rel="noreferrer">Tavily</a></h2>
        <p>面向 AI Agent 的 Web 访问层，覆盖搜索、内容提取、站点 Map/Crawl 与 Research。</p>
      </div>
    </article>
    <article class="web-product-card web-product-firecrawl">
      <div class="web-product-copy">
        <h2><a href="https://www.firecrawl.dev/" target="_blank" rel="noreferrer">Firecrawl</a></h2>
        <p>面向 AI 的 Web 数据 API，把搜索结果或网页转成 Markdown、JSON 等内容，并支持整站 Crawl。</p>
      </div>
    </article>
    </div>
    <div class="web-products-meta">
      <div class="web-related-products">
        <span>其他产品</span>
        <p><a href="https://exa.ai/" target="_blank" rel="noreferrer">Exa</a>、<a href="https://api.search.brave.com/app/documentation/web-search/get-started" target="_blank" rel="noreferrer">Brave</a>、<a href="https://www.tinyfish.ai/" target="_blank" rel="noreferrer">TinyFish</a></p>
      </div>
      <div class="web-products-integration">
        <span class="web-products-integration-heading">接入方式</span>
        <strong>MCP</strong>
        <span class="web-products-integration-separator">/</span>
        <strong>Skill + CLI</strong>
      </div>
    </div>
</div>

---

<div class="editorial-slide browser-page">
  <h1 class="title">浏览器自动化</h1>
  <p class="lead">先区分调试、测试和长期任务执行，再选择对应的浏览器工具。</p>
  <div class="browser-layout">
    <div class="browser-tools">
      <div class="browser-tool"><h3><a href="https://github.com/ChromeDevTools/chrome-devtools-mcp" target="_blank" rel="noreferrer">Chrome DevTools MCP / CLI</a></h3><p>偏开发调试，直接使用 Console、Network、Performance 和页面检查能力。</p></div>
      <div class="browser-tool"><h3><a href="https://github.com/microsoft/playwright-mcp" target="_blank" rel="noreferrer">Playwright MCP / CLI</a></h3><p>偏浏览器自动化，执行页面访问、点击、输入和 UI 测试。</p></div>
    </div>
    <div class="browser-comparison">
      <div class="browser-route browser-route-harness">
        <div class="browser-route-name"><strong><a href="https://github.com/browser-use/browser-harness" target="_blank" rel="noreferrer">Browser Harness</a></strong></div>
        <div class="browser-route-copy"><p>可扩展的浏览器执行层，适合个人 Agent、内部工具和长尾网站。</p><b>需要可长期演进的浏览器能力</b></div>
      </div>
      <div class="browser-route browser-route-cli">
        <div class="browser-route-name"><strong><a href="https://github.com/vercel-labs/agent-browser" target="_blank" rel="noreferrer">agent-browser</a></strong></div>
        <div class="browser-route-copy"><p>标准化浏览器 CLI，适合 AI Coding、前端验收和 E2E。</p><b>主要执行 AI Coding 中的网页操作</b></div>
      </div>
      <div class="browser-route browser-route-use">
        <div class="browser-route-name"><strong><a href="https://github.com/browser-use/browser-use" target="_blank" rel="noreferrer">Browser Use</a></strong></div>
        <div class="browser-route-copy"><p>任务级 Browser Agent 框架，适合构建浏览器 Agent 产品与任务自动化。</p><b>要构建完整的 Browser Agent 产品</b></div>
      </div>
    </div>
  </div>
</div>

---

<div class="editorial-slide">
  <h1 class="title">Skill的安装和管理</h1>
  <p class="lead">从目录发现并安装 Skill，再统一维护不同 Agent 的能力配置。</p>
  <div class="manager-layout">
    <div class="manager-column">
      <h2><a href="https://skills.sh/" target="_blank" rel="noreferrer">skills.sh</a></h2>
      <p>开放的 Agent Skills 目录与排行榜，用于发现和安装可复用的任务能力。</p>
      <ul class="bullet-list">
        <li>按 Trending、Hot、Official 等分类发现社区 Skills。</li>
        <li>选定 Skill 后，用 Skills CLI 安装到指定 Agent。</li>
      </ul>
      <div class="manager-command"><a href="https://www.skills.sh/docs/cli" target="_blank" rel="noreferrer">npx skills add &lt;owner/repo&gt;</a></div>
    </div>
    <div class="manager-column">
      <h2><a href="https://github.com/xingkongliang/skills-manager" target="_blank" rel="noreferrer">Skills Manager</a></h2>
      <p>跨平台桌面管理工具，提供统一 Skill 库、跨 Agent 部署、Preset 管理、版本更新和 Git 备份同步。</p>
      <ul class="bullet-list">
        <li>统一管理不同来源的 Skills。</li>
        <li>跨 Agent、跨项目部署，并保留版本和备份恢复路径。</li>
      </ul>
    </div>
  </div>
</div>

---

<div class="editorial-slide">
  <h1 class="title">Agent 会话管理</h1>
  <p class="lead">长任务需要状态可观察、可交接、可恢复。</p>
  <div class="session-layout"><div class="session-column"><h2><a href="https://github.com/herdrdev/herdr" target="_blank" rel="noreferrer">Herdr</a></h2><p>让多个 Agent 同时工作，并且能够被观察、组织和协作。Herdr 通过后台 Session Server 持有真实终端进程。</p><ul class="bullet-list"><li><strong>Agent 状态感知：</strong>识别 working、blocked、done 和 idle 状态。</li><li><strong>持久化 Session：</strong>关闭窗口或断开连接后，任务仍可继续运行。</li><li><strong>多 Agent 工作区：</strong>用 Workspace、Tab 和 Pane 管理多个项目与多个 Agent。</li><li><strong>Agent 协作：</strong>通过共享工作区、终端状态、脚本或 API 协调并行任务。</li></ul></div><div class="session-column"><h2><a href="https://github.com/stablyai/orca" target="_blank" rel="noreferrer">Orca</a></h2><p>面向多 Agent 开发的桌面 IDE，将多个 Agent 与开发工具集中到一个工作台。</p><ul class="bullet-list"><li><strong>独立 Worktree：</strong>每个 Agent 使用独立 Git Worktree，便于并行开发、比较结果和合并代码。</li><li><strong>内置浏览器：</strong>提供 Chromium 浏览器与 Design Mode，可将页面元素直接交给 Agent。</li><li><strong>文件与终端：</strong>提供文件管理器、编辑器和终端分屏，减少工具切换。</li><li><strong>代码审查：</strong>集成 Diff 查看、标注、提交和推送，方便从生成到交付。</li></ul></div></div>
</div>

---

<div class="editorial-slide chapter-page">
  <div class="chapter-index">第四章</div>
  <div class="chapter-copy">
    <h1>AI Coding 工作流</h1>
    <p>从 Prompt 走向目标、环境、验证和交付的完整路径。</p>
  </div>
</div>

---

<div class="editorial-slide">
  <h1 class="title">Agent配置目录结构</h1>
  <div class="code-layout directory-layout">
    <div class="directory-board">
      <div class="directory-board-title">Claude Code</div>
      <pre class="directory-tree"><span class="directory-heading">用户级目录</span>  <span class="directory-path">~/.claude/</span>&#10;<span class="directory-context">├── CLAUDE.md</span>&#10;<span class="directory-settings">├── settings.json</span>&#10;<span class="directory-skills">├── skills/</span>&#10;<span class="directory-agent">└── agents/*.md</span>&#10;&#10;<span class="directory-heading">项目根目录</span>  <span class="directory-path">/repo</span>&#10;<span class="directory-context">├── CLAUDE.md</span>&#10;<span class="directory-local">├── CLAUDE.local.md</span>&#10;<span class="directory-mcp">├── .mcp.json</span>&#10;<span class="directory-folder">└── .claude/</span>&#10;<span class="directory-settings">    ├── settings.json</span>&#10;<span class="directory-local">    ├── settings.local.json</span>&#10;<span class="directory-rules">    ├── rules/*.md</span>&#10;<span class="directory-skills">    ├── skills/</span>&#10;<span class="directory-agent">    └── agents/*.md</span></pre>
    </div>
    <div class="directory-board">
      <div class="directory-board-title">.agents（支持主流Agent）</div>
      <pre class="directory-tree"><span class="directory-heading">用户级目录</span>  <span class="directory-path">~/.agents/</span>&#10;<span class="directory-skills">└── skills/</span>&#10;&#10;<span class="directory-heading">项目级目录</span>  <span class="directory-path">repo/</span>&#10;<span class="directory-context">├── AGENTS.md</span>&#10;<span class="directory-folder">└── .agents/</span>&#10;<span class="directory-skills">    └── skills/</span></pre>
    </div>
    <div class="directory-note">
      <div><strong class="directory-note-agent">AGENTS.md</strong>：<strong class="directory-note-reuse">@CLAUDE.md</strong> 的内容，实现复用；<br /><strong class="directory-note-skill">skills/</strong>：直接软链接</div>
    </div>
  </div>
</div>

---

<div class="editorial-slide project-context-page prompt-only-page">
  <h1 class="title">全局/项目级长期上下文</h1>
  <div class="prompt-context-layout">
    <section class="system-prompt-card">
    <div class="system-prompt-heading"><h2>CLAUDE.md / AGENTS.md</h2><span>提示词文件</span></div>
    <div class="system-prompt-principles">
      <article><strong>少而重要</strong><p>只保留每个 Session 都值得加载的信息，并控制在 200 行以内。</p></article>
      <article><strong>写不可推断的信息</strong><p>记录项目架构、特殊约定、工具命令、历史包袱和踩坑点，不复述代码。</p></article>
      <article><strong>分层组织</strong><p>Root CLAUDE.md 管全局，子目录 CLAUDE.md / Rules 管局部。</p></article>
      <article><strong>渐进披露</strong><p>复杂流程放进 Skill，按任务需要加载。</p></article>
      <article><strong>能强制的交给工具</strong><p>格式化、检查和禁止操作等确定性要求交给 Hooks / Permissions。</p></article>
    </div>
    <div class="system-prompt-compat"><strong>兼容性</strong><span>Claude Code 读取 <code>CLAUDE.md</code>；需要兼容其他 Agent 时，可在首行写 <code>@AGENTS.md</code>，或直接建立软链接。</span></div>
    </section>
    <section class="rules-card">
      <div class="rules-card-heading"><h2>Rules</h2><span>路径级规则</span></div>
      <ul class="system-prompt-rules"><li><b>按主题拆分</b>：前端、后端、测试、安全等规则分开维护，避免一个 Rule 文件越来越大。</li><li><b>按路径生效</b>：能限定目录或文件类型的规则就限定范围，减少无关加载。</li><li><b>项目优先</b>：项目规则放项目内，全局只保留真正跨项目通用的规则。</li><li><b>持续治理</b>：定期清理重复、过时、冲突的 Rules，避免和 CLAUDE.md、Skills 互相打架。</li></ul>
    </section>
  </div>
</div>

---

<div class="editorial-slide capability-management-page">
  <h1 class="title">能力扩展</h1>
  <div class="capability-focus-grid">
    <article class="context-management-card context-management-skill"><h2>Skills 管理</h2><ul class="context-management-list"><li><strong>按需安装</strong><span>需要什么装什么，不做全量预装。</span></li><li><strong>分层管理</strong><span>通用能力放全局，项目专属能力放项目内。</span></li><li><strong>持续治理</strong><span>定期清理重复、过时、低使用的 Skill。</span></li></ul></article>
    <article class="context-management-card context-management-mcp"><h2>MCP 管理</h2><ul class="context-management-list"><li><strong>分层配置</strong><span>区分项目级和全局级，<b>优先项目级</b>，避免污染所有项目。</span></li><li><strong>尽量少用</strong><span>能用 Agent 原生能力、CLI、API 解决的，就不要额外挂 MCP。</span></li><li><strong>控制数量</strong><span>减少重复和低价值 MCP，降低依赖、权限和稳定性成本。</span></li></ul></article>
  </div>
  <div class="capability-secondary-grid">
    <article class="capability-secondary-card capability-hooks"><h2>Hooks</h2><p class="capability-one-line">把格式化、Lint、检查和危险操作等确定性动作交给 Hook。</p></article>
    <article class="capability-secondary-card capability-lsp"><h2>LSP / Code Intelligence</h2><p class="capability-one-line">为大型代码库提供跳转、引用和类型诊断等代码智能，按语言和项目配置。</p></article>
    <article class="capability-secondary-card capability-subagents"><h2>Subagents</h2><p class="capability-one-line">将搜索、Review、Research 等独立任务交给子 Agent，实现上下文隔离与并行执行。</p></article>
  </div>
</div>

---

<div class="editorial-slide">
  <h1 class="title">如何写一个 Skill</h1>
  <div class="skill-practice-list">
    <article class="skill-practice-item"><strong class="skill-practice-number">01</strong><div><h2>选择真实任务</h2><p>从重复工作中选择一个需求，先让 Agent 完成任务，得到满意的结果。</p></div></article>
    <article class="skill-practice-item"><strong class="skill-practice-number">02</strong><div><h2>整理执行经验</h2><p>记录可复用的步骤、所需资料和工具，以及执行中需要反复提醒的要求。</p></div></article>
    <article class="skill-practice-item"><strong class="skill-practice-number">03</strong><div><h2>编写 Skill</h2><p>写清操作步骤，将固定操作整理成脚本，附上模板或示例，并明确结果检查和错误修复方法。</p></div></article>
    <article class="skill-practice-item"><strong class="skill-practice-number">04</strong><div><h2>测试效果</h2><p>使用不同任务和模型测试，检查结果是否达标，找出容易失败的环节。</p></div></article>
    <article class="skill-practice-item"><strong class="skill-practice-number">05</strong><div><h2>持续改进</h2><p>根据实际使用和分享后的反馈修改，优先解决共性问题，避免堆叠特殊需求。</p></div></article>
  </div>
</div>

---

<div class="editorial-slide">
  <h1 class="title">Superpowers 与 mattpocock</h1>
  <div class="workflow-methods sdd-methods">
    <div class="method-column"><h2><a href="https://github.com/obra/superpowers" target="_blank" rel="noreferrer">Superpowers</a></h2><p>通过 Sub-Agent、TDD、Review 和可选的 Git Worktree，提高交付质量。</p><div class="method-flow method-arrow-flow method-arrow-flow-five"><span>brainstorming：头脑风暴</span><b class="method-arrow">→</b><span>plan：编写计划</span><b class="method-arrow">→</b><span>execute：执行</span><b class="method-arrow">→</b><span>review：审查</span><b class="method-arrow">→</b><span>finish：收尾</span></div></div>
    <div class="method-column"><h2><a href="https://github.com/mattpocock/skills" target="_blank" rel="noreferrer">mattpocock/skills</a></h2><p>用一组 Skills 把需求澄清、Spec、任务拆分、实现和审查串起来。</p><div class="method-flow method-arrow-flow method-arrow-flow-five"><span>grill-with-docs：需求澄清</span><b class="method-arrow">→</b><span>to-spec：生成 Spec</span><b class="method-arrow">→</b><span>to-tickets：拆分任务</span><b class="method-arrow">→</b><span>implement：实现</span><b class="method-arrow">→</b><span>code-review：代码审查</span></div></div>
  </div>
</div>

---

<div class="editorial-slide sdd-page">
  <h1 class="title">SDD</h1>
  <p class="lead">SDD（Spec-Driven Development，规范驱动开发）：以规格说明为核心，先明确要构建什么，再让 Agent 根据规格完成设计、拆解和实现。</p>
  <div class="workflow-methods sdd-methods">
    <div class="method-column">
      <h2><a href="https://github.com/Fission-AI/OpenSpec" target="_blank" rel="noreferrer">OpenSpec</a>：设计与变更契约</h2>
      <p>轻量、流程清晰（propose → apply → sync/archive）；规范与代码同仓，持续维护当前系统行为的主规范。</p>
      <div class="method-flow method-arrow-flow"><span>propose：提出变更</span><b class="method-arrow">→</b><span>review / update：评审修改</span><b class="method-arrow">→</b><span>apply：开始实现</span><b class="method-arrow">→</b><span>archive：归档记录</span></div>
    </div>
    <div class="method-column">
      <h2><a href="https://github.com/github/spec-kit" target="_blank" rel="noreferrer">Spec Kit</a>：规范驱动流程</h2>
      <p>功能更强、扩展性更高，支持预设、扩展和工作流；但标准流程更复杂，规范归档需要额外组织。</p>
      <div class="method-flow method-arrow-flow"><span>Spec：明确需求</span><b class="method-arrow">→</b><span>Plan：制定方案</span><b class="method-arrow">→</b><span>Tasks：拆分任务</span><b class="method-arrow">→</b><span>Implement：开始实现</span></div>
    </div>
  </div>
</div>

---

<div class="editorial-slide">
  <h1 class="title">AI工程化</h1>
  <div class="paradigm-layout"><div class="paradigm-row"><h3>Prompt Engineering</h3><p>关注“怎么写好一条指令”。</p></div><div class="paradigm-row"><h3>Context Engineering</h3><p>关注“怎么给 AI 提供足够且精准的上下文”。</p></div><div class="paradigm-row"><h3>Harness Engineering</h3><p>关注“怎么构建一个系统性的框架来约束和驱动 AI”。</p></div><div class="paradigm-row"><h3>Loop Engineering</h3><p>关注“怎么让 Agent 持续执行、验证并在失败后自我修正”。</p></div><div class="paradigm-row"><h3>Graph Engineering</h3><p>关注“怎么把 Agent、工具和流程编排成可分支、可并行的协作网络”。</p></div></div>
</div>

---

<div class="editorial-slide chapter-page">
  <div class="chapter-index">第五章</div>
  <div class="chapter-copy">
    <h1>思考</h1>
  </div>
</div>

---

<div class="editorial-slide meta-capability-page">
  <h1 class="title">Agent 元能力：善于借助 Agent 解决问题</h1>
  <p class="meta-capability-intro">从善用搜索引擎、善用网页 Chat，到善用 Agent，解决问题的方式正在从“获取答案”走向“直接完成任务”。</p>
  <div class="meta-capability-grid">
    <article class="meta-capability-card meta-capability-install"><div class="meta-capability-number">01</div><div><h2>先装一个能用的 Agent</h2><p>先有一个真正能干活的 Agent，后面的配置、扩展和使用才有基础。</p></div></article>
    <article class="meta-capability-card meta-capability-equip"><div class="meta-capability-number">02</div><div><h2>用 Agent 武装 Agent</h2><p>环境配置、工具安装、能力接入，都可以让 Agent 参与解决；逐步补齐浏览器、终端、CLI、MCP、Skill 等“手、眼、脚”。</p></div></article>
    <article class="meta-capability-card meta-capability-explore"><div class="meta-capability-number">03</div><div><h2>善用 Agent 解决陌生问题</h2><p>遇到不会的、没做过的、复杂的问题，也敢于先让 Agent 尝试，善于借助它探索方法、解决阻塞，不断扩展自己能解决的问题边界。</p></div></article>
    <article class="meta-capability-card meta-capability-build"><div class="meta-capability-number">04</div><div><h2>用 Agent 构建自己的工具</h2><p>把重复需求和个人工作方式做成 Skill、脚本、小工具、浏览器插件、客户端或自动化流程，让 Agent 不只是现成工具，也能帮你创造新的工具。</p></div></article>
  </div>
  <div class="meta-capability-conclusion"><span>核心变化</span><strong>从“会使用 Agent”，走向“善于借助 Agent 持续扩展自己的问题解决能力”。</strong></div>
</div>

---

<div class="editorial-slide thinking-methods-page">
  <h1 class="title">AI 编程中的思维方式</h1>
  <p class="thinking-methods-subtitle">用成熟的思维框架，让问题更清晰、验证更可靠。</p>
  <div class="thinking-method-list">
    <article class="thinking-method-card thinking-method-first">
      <h2>第一性原理</h2>
      <p>先回到问题本身。从目标、事实和约束出发，确认问题是否真实存在、能否复现，再判断根因和解决方案，避免 Agent 一上来就执行，却在错误的问题上越走越远。</p>
    </article>
    <article class="thinking-method-card thinking-method-adversarial">
      <h2>对抗式审查</h2>
      <p>主动引入一个反方，让另一个 Agent 从独立视角寻找漏洞、反例、遗漏和失败场景。不是让多个 Agent 相互附和，而是通过交叉审查提高结论可信度。</p>
    </article>
    <article class="thinking-method-card thinking-method-ablation">
      <h2>消融实验</h2>
      <p>拿掉一个变量，看结果是否变化。某条 Rule、某个 Skill、Tool 或 Prompt 到底有没有价值，不靠感觉判断；保持其他条件不变，删除后重新运行，用结果验证它是否真的有效。</p>
    </article>
    <article class="thinking-method-card thinking-method-razor">
      <h2>奥卡姆剃刀</h2>
      <p>优先选择最简单、能工作的方案。能用简单方案解决，就不要过早引入复杂架构；先完成最小可行闭环，再根据真实需求逐步演进，避免过度设计。</p>
    </article>
    <article class="thinking-method-card thinking-method-uncertainty">
      <h2>不确定性显式化</h2>
      <p>让不确定性显式出现，要求 Agent 主动说明：哪些结论缺少证据、哪些场景尚未验证、哪些判断只是推测，把隐藏的不确定性变成下一步可以验证的问题。</p>
    </article>
  </div>
  <div class="thinking-methods-conclusion">好的思维框架，可以用很少的 Prompt，激活一整套分析、质疑与验证机制。</div>
</div>

---

<div class="editorial-slide engineering-map-page">
  <div class="engineering-title-row"><h1 class="title">使用 Coding Agent <span class="engineering-title-note">AI 工程能力</span></h1></div>
  <p class="engineering-map-intro">Coding Agent 正在改变软件开发中人的工作重心：</p>
  <div class="engineering-transition-graphic"><span class="engineering-transition-from">亲自实现代码</span><b>→</b><span class="engineering-transition-to">决定做什么、设计架构、定义 Spec、组织执行和验证结果</span></div>
  <div class="engineering-workflow-grid">
    <section class="engineering-process">
      <div class="engineering-section-heading"><strong>基本工作流</strong></div>
      <div class="engineering-map-steps">
        <article class="engineering-map-step engineering-map-step-plan"><strong>01</strong><div><h3>Planning</h3><p>理解问题、设计架构、明确 Spec 与执行计划。</p></div></article>
        <article class="engineering-map-step engineering-map-step-build"><strong>02</strong><div><h3>Execution</h3><p>Agent 构建、测试、验证和修复。</p></div></article>
        <article class="engineering-map-step engineering-map-step-ship"><strong>03</strong><div><h3>Deployment &amp; Monitoring</h3><p>部署、监控、发现问题并持续迭代。</p></div></article>
        <article class="engineering-map-step engineering-map-step-feedback"><strong>04</strong><div><h3>Feedback</h3><p>根据结果反馈调整计划与执行，进入下一轮闭环。</p></div></article>
      </div>
    </section>
    <section class="engineering-human">
      <div class="engineering-section-heading"><strong>核心能力</strong><span>驾驭 Coding Agent，放大个人与团队的生产力</span></div>
      <div class="engineering-capability-grid">
        <article class="engineering-capability engineering-capability-guide"><h3>工作流管理</h3><p>决定如何拆解、执行与迭代任务。</p></article>
        <article class="engineering-capability engineering-capability-autonomy"><h3>Agent 自主性</h3><p>控制 Agent 的自主程度、Context 与多 Agent 协作。</p></article>
        <article class="engineering-capability engineering-capability-review"><h3>结果审查</h3><p>通过测试、Evals、Code Review 等验证输出。</p></article>
        <article class="engineering-capability engineering-capability-custom"><h3>Agent 与环境定制</h3><p>通过 Skills、MCP、Hooks、AGENTS.md 等增强能力。</p></article>
        <article class="engineering-capability engineering-capability-core"><h3>Agent 基础原理</h3><p>理解 LLM、Harness、Context、Tools、Subagents 等机制。</p></article>
      </div>
    </section>
  </div>
  <div class="engineering-practice-bar"><span>高效使用 Coding Agent，不是单纯追求更高自主性，而是建立“<strong class="engineering-loop-step engineering-loop-plan">规划</strong> → <strong class="engineering-loop-step engineering-loop-build">执行</strong> → <strong class="engineering-loop-step engineering-loop-review">验证</strong> → <strong class="engineering-loop-step engineering-loop-feedback">反馈</strong>”的工程闭环。</span></div>
</div>

---

<div class="editorial-slide silver-bullet-page">
  <div class="silver-bullet-header">
    <div>
      <h1 class="title">AI不是软件工程的银弹</h1>
      <p class="silver-bullet-subtitle">只有能让软件生产率、可靠性和简洁性提升一个数量级的方法，才称得上“银弹”。</p>
    </div>
  </div>

  <div class="silver-bullet-columns">
    <section class="silver-bullet-column silver-bullet-essential">
      <div class="silver-bullet-column-head">
        <div><h2>软件工程的本质困难</h2><p>它们不是“写代码慢”，也不会被 AI 自动消除</p></div>
      </div>
      <div class="silver-bullet-list">
        <article><strong>目标与概念</strong><p>要解决什么、为什么解决，以及什么才算成功。</p></article>
        <article><strong>复杂性</strong><p>业务规则、状态、依赖和边界相互交织。</p></article>
        <article><strong>约束与一致性</strong><p>系统必须适配既有架构、规范、法规和组织约束。</p></article>
        <article><strong>变化与验证</strong><p>需求持续变化，正确性还要靠测试、运行反馈和长期维护确认。</p></article>
      </div>
    </section>
    <section class="silver-bullet-column silver-bullet-accidental">
      <div class="silver-bullet-column-head">
        <div><h2>AI 能解决 / 缓解的部分</h2><p>不是消灭复杂性，而是让 AI 直接承接复杂实现</p></div>
      </div>
      <div class="silver-bullet-list">
        <article><strong>自主执行</strong><p>从任务描述出发，规划、编码、运行、调试并交付。</p></article>
        <article><strong>复杂度承接</strong><p>理解并修改大范围代码，把实现复杂性转交给 Code Agent。</p></article>
        <article><strong>流程压缩</strong><p>串联规划、开发、测试和文档，减少传统协作中的等待。</p></article>
        <article><strong>并行探索</strong><p>同时尝试多种方案，持续迭代，放大个人和小团队的执行规模。</p></article>
      </div>
    </section>
  </div>

  <div class="silver-bullet-boundary">
    <div class="silver-bullet-boundary-item silver-bullet-cannot">
      <span>AI 不能替代</span><strong>目标与价值、架构取舍、组织共识、验收责任</strong>
    </div>
    <div class="silver-bullet-boundary-item silver-bullet-can">
      <span>AI 主要解决</span><strong>复杂实现、重复执行、调试迭代、并行探索</strong>
    </div>
  </div>

  <div class="silver-bullet-conclusion">AI 放大了处理软件复杂性的能力，但没有让复杂性本身消失——所以它仍然不是软件工程的银弹。</div>
</div>
