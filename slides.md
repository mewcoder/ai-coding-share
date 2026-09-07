---
theme: default
title: AI Coding：从原理到实践
aspectRatio: 16/9
canvasWidth: 1280
transition: fade
mdc: true
---

<div class="editorial-slide cover">
  <div class="cover-left">
    <h1><span class="cover-title-en">AI Coding</span><span class="cover-title-cn">从原理到实践</span></h1>
    <div class="cover-rule"></div>
    <p class="cover-subtitle">从 AI Coding 的发展历程出发，了解 Agent 的基本原理与运行机制，认识 Coding Agent 的工具链，并探索适合个人与团队的工作流实践。</p>
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
    <div class="toc-row"><strong>五</strong><h3>实践与思考</h3></div>
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
        <span>Grok 4.6</span><span>DeepSeek V4 Pro</span>
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
  </div>
</div>

---

<div class="editorial-slide">
  <h1 class="title">开发环境准备</h1>
  <p class="lead">路径、权限、依赖和验证命令稳定，Agent 才有可靠的落点。</p>
  <div class="environment-layout">
    <div class="environment-column"><h2>基础环境</h2><div class="environment-item"><h3>PowerShell 7</h3><p>Windows 下更现代的 Shell，适合日常开发、脚本和 CLI Agent。</p></div><div class="environment-item"><h3>Windows Terminal</h3><p>统一承载多标签和分屏，方便管理多个会话。</p></div><div class="environment-item"><h3>Node.js 22+</h3><p>许多 AI Coding CLI、MCP Server 和 npm 工具的运行环境。</p></div><div class="environment-item"><h3>Python 3+</h3><p>自动化、数据处理和脚本工具常见的运行环境。</p></div></div>
    <div class="environment-column"><h2>工程基础</h2><div class="environment-item"><h3>Git</h3><p>版本控制、分支管理和变更追踪，保留恢复路径。</p></div><div class="environment-item"><h3>WSL</h3><p>可选的 Linux 环境，适合 Docker、Linux Shell 和部分 MCP 工具。</p></div><div class="environment-item"><h3>推荐组合</h3><p>Windows Terminal、PowerShell 7、Node.js 22+ 和 Python 3+，WSL 按需安装。</p></div></div>
  </div>
  <div class="environment-bottom">先让 Agent 能稳定运行，再讨论它能完成多复杂的任务。</div>
</div>

---

<div class="editorial-slide tool-page">
  <div class="tool-name"><h1>CLI</h1><div class="tool-role">终端是工作面</div></div>
  <div class="tool-content"><h2>适合命令驱动的开发方式</h2><div class="tool-row"><h3>代表工具</h3><p class="tool-links">Claude Code、OpenCode、OpenCode 2、Pi Coding Agent、OMP、Codex CLI</p></div><div class="tool-row"><h3>工作特点</h3><p>贴近 Shell、脚本和远程环境，适合连续执行、自动化和可复现命令。</p></div><div class="tool-row"><h3>使用判断</h3><p>当任务需要频繁读写文件、运行测试或串接命令时，终端工作面更直接。</p></div></div>
</div>

---

<div class="editorial-slide tool-page">
  <div class="tool-name"><h1>IDE</h1><div class="tool-role">代码与对话在同一工作面</div></div>
  <div class="tool-content"><h2>适合需要持续查看代码和 Diff 的开发方式</h2><div class="tool-row"><h3>代表工具</h3><p class="tool-links">Cursor、Qoder、CodeBuddy、Trae</p></div><div class="tool-row"><h3>工作特点</h3><p>代码、变更、对话和运行结果在编辑器内持续展开，适合边看边改。</p></div><div class="tool-row"><h3>使用判断</h3><p>当开发者需要频繁审阅局部变更、文件关联和界面反馈时，IDE 更顺手。</p></div></div>
</div>

---

<div class="editorial-slide tool-page">
  <div class="tool-name"><h1>App</h1><div class="tool-role">任务与会话的工作台</div></div>
  <div class="tool-content"><h2>适合并行协作和状态查看</h2><div class="tool-row"><h3>代表工具</h3><p class="tool-links">Codex、WorkBuddy、Qoder Work、Trae Work</p></div><div class="tool-row"><h3>工作特点</h3><p>把对话、任务、会话和交付状态放在更完整的工作台中。</p></div><div class="tool-row"><h3>使用判断</h3><p>当任务需要异步运行、并行推进、交接或 Review 时，平台态更合适。</p></div></div>
</div>

---

<div class="editorial-slide">
  <h1 class="title">Agent 配置与目录结构</h1>
  <p class="lead">以 Claude Code 为例，配置分为用户级和项目级，分别服务个人复用与团队协作。</p>
  <div class="code-layout">
    <pre class="code-block">用户级目录
~/.claude/
├── CLAUDE.md
├── settings.json
└── skills/{name}/SKILL.md
项目根目录
├── CLAUDE.md
├── .mcp.json
└── .claude/
    ├── settings.json
    ├── settings.local.json
    ├── rules/*.md
    ├── skills/{name}/SKILL.md
    └── agents/*.md</pre>
    <div class="explanation"><h2>配置的分工</h2><div class="explanation-row"><h3>指令与规则</h3><p>CLAUDE.md 提供持续上下文，rules 按主题或文件路径拆分规则。</p></div><div class="explanation-row"><h3>设置与能力</h3><p>settings.json 配置运行行为，MCP 接入工具，Skills 按任务需要加载。</p></div><div class="explanation-row"><h3>权限边界</h3><p>这些文件是用户补充的上下文和配置，不等同于完整系统提示词，也不能代替权限控制。</p></div></div>
  </div>
</div>

---

<div class="editorial-slide">
  <h1 class="title">CC Switch：配置切换与 API 代理</h1>
  <p class="lead">把 Provider、Model、API Key 和 Base URL 从项目逻辑中隔离出来。</p>
  <div class="flow-line"><div class="flow-cell"><h3>Coding Agent</h3><p>Claude Code、Codex、OpenCode 等工具。</p></div><div class="flow-connector"></div><div class="flow-cell"><h3>CC Switch</h3><p>统一切换 Provider、Model、代理、MCP 与 Skills。</p></div><div class="flow-connector"></div><div class="flow-cell"><h3>Provider 与 Model</h3><p>不同服务入口、API Key 和 Base URL。</p></div></div>
  <div class="rule-list" style="margin-top: 44px"><div class="rule-item"><h3>解决的问题</h3><p>不同 Coding Agent 的连接配置彼此分散，切换和维护成本较高。</p></div><div class="rule-item"><h3>工具定位</h3><p>CC Switch 是 Coding Agent 的配置管理、切换与 API 代理工具。</p></div></div>
</div>

---

<div class="editorial-slide">
  <h1 class="title">常见 API 格式</h1>
  <p class="lead">URL 相似，不代表消息契约相同。接入时要确认消息结构、工具调用、流式事件和状态续接方式。</p>
  <div class="api-table" style="margin-top: 36px"><div class="tool-row"><h3>OpenAI Chat Completions</h3><p><code>POST /v1/chat/completions</code><br />以 messages 为中心，每轮请求通常携带完整消息历史。</p></div><div class="tool-row"><h3>Anthropic Messages</h3><p><code>POST /v1/messages</code><br />以 system、messages、内容块和工具定义组织请求。</p></div><div class="tool-row"><h3>OpenAI Responses</h3><p><code>POST /v1/responses</code><br />通过 previous_response_id 关联上一轮，减少重复传递。</p></div></div>
</div>

---

<div class="editorial-slide">
  <h1 class="title">9Router：统一模型网关</h1>
  <p class="lead">9Router 位于 Coding Agent 与模型之间，负责入口、路由、降级与协议适配。</p>
  <div class="flow-line"><div class="flow-cell"><h3>调用方</h3><p>Coding Agent、业务脚本和工具。</p></div><div class="flow-connector"></div><div class="flow-cell"><h3>9Router</h3><p>统一入口、Provider 路由与故障切换。</p></div><div class="flow-connector"></div><div class="flow-cell"><h3>模型服务</h3><p>不同 Provider、Model 和协议。</p></div></div>
  <div class="capability-list"><div class="capability"><h3>统一入口</h3><p>减少接入差异。</p></div><div class="capability"><h3>模型路由</h3><p>按任务选择模型。</p></div><div class="capability"><h3>Failover</h3><p>服务异常时保留路径。</p></div><div class="capability"><h3>配额用量</h3><p>记录调用与消耗。</p></div><div class="capability"><h3>协议适配</h3><p>隔离上游差异。</p></div></div>
</div>

---

<div class="editorial-slide tool-page">
  <div class="tool-name"><h1>Tavily</h1><div class="tool-role">偏 Search 与 Research</div></div>
  <div class="tool-content"><h2>面向 Agent 的搜索与研究接口</h2><div class="tool-row"><h3>主要能力</h3><p>Web Search、Extract、Crawl、Research。</p></div><div class="tool-row"><h3>适合任务</h3><p>资料搜索、文档查询、技术调研，以及把搜索结果交给下一步 Agent。</p></div><div class="tool-row"><h3>接入方式</h3><p>支持 MCP，也可以通过 CLI 与 Skills 接入。</p></div><div class="tool-row"><h3>实践判断</h3><p>先约束查询边界，再决定哪些来源、摘要和线索值得带回 Context。</p></div></div>
</div>

---

<div class="editorial-slide tool-page">
  <div class="tool-name"><h1>Firecrawl</h1><div class="tool-role">偏 Fetch 与 Crawl</div></div>
  <div class="tool-content"><h2>把网页转换成下游可以消费的内容</h2><div class="tool-row"><h3>主要能力</h3><p>Search、Scrape、Crawl、Extract。</p></div><div class="tool-row"><h3>适合任务</h3><p>知识采集、站点级抓取、动态网页处理和批量提取。</p></div><div class="tool-row"><h3>接入方式</h3><p>支持 MCP，也可以通过 CLI 与 Skills 接入。</p></div><div class="tool-row"><h3>实践判断</h3><p>先分清单页抓取还是多页爬取，再设计范围、频率、落盘和失败降级。</p></div></div>
</div>

---

<div class="editorial-slide">
  <h1 class="title">Web Search 与 Web Fetch 的接入方式</h1>
  <p class="lead">同一项外部能力，可以通过协议接入，也可以通过命令和方法包接入。</p>
  <div class="web-layout"><div class="web-column"><h2>MCP</h2><p>直接作为 Agent 的 Tools 使用，适合统一发现能力并返回结构化结果。</p><ul class="bullet-list"><li>Agent 发现工具描述和参数 Schema。</li><li>调用搜索、抓取或抽取能力。</li><li>把结果写回 Context，支撑下一步判断。</li></ul></div><div class="web-column"><h2>CLI + Skills</h2><p>Agent 通过命令行调用，Skill 负责说明使用方法、参数和流程。</p><ul class="bullet-list"><li>Skill 沉淀常用命令和任务方法。</li><li>CLI 连接具体服务或脚本。</li><li>适合内网或受限环境中的组合方案。</li></ul></div></div>
</div>

---

<div class="editorial-slide">
  <h1 class="title">浏览器自动化</h1>
  <p class="lead">先区分调试、测试和长期任务执行，再选择对应的浏览器工具。</p>
  <div class="browser-layout"><div class="image-panel browser-image"><img src="/images/browser-agent-comparison.png" alt="浏览器工具与框架对比" /></div><div class="browser-tools"><div class="browser-tool"><h3>Chrome DevTools MCP</h3><p>面向开发调试，提供 Console、Network、Performance 和页面检查能力。</p></div><div class="browser-tool"><h3>Playwright MCP</h3><p>面向浏览器自动化，提供页面访问、点击、输入和 UI 测试能力。</p></div><div class="browser-tool"><h3>Agent 浏览器工具与框架</h3><p>通过 CLI、MCP 或 Skill 暴露给 Agent，承担任务执行和长期自动化。</p></div></div></div>
</div>

---

<div class="editorial-slide">
  <h1 class="title">Skill Manager：让方法包可发现、可部署</h1>
  <p class="lead">Skill 规模变大后，也需要来源、版本、适用范围和回滚方式。</p>
  <div class="manager-layout"><div class="manager-column"><h2>Skills Manager</h2><p>跨平台桌面管理工具，提供统一 Skill 库、跨 Agent 部署、Preset 管理、版本更新和 Git 备份同步。</p><ul class="bullet-list"><li>统一管理不同来源的 Skills。</li><li>跨 Agent、跨项目部署。</li><li>通过版本和备份保留恢复路径。</li></ul></div><div class="manager-column"><h2>skills.sh</h2><p>开放的 Agent Skills 目录与排行榜。</p><ul class="bullet-list"><li>搜索和发现社区 Skills。</li><li>查看 Trending、Hot 和 Official 分类。</li><li>安装可复用的任务能力。</li></ul><div class="manager-command">npx skills add {owner}/{repo}</div></div></div>
</div>

---

<div class="editorial-slide">
  <h1 class="title">Agent 会话管理</h1>
  <p class="lead">长任务需要状态可观察、可交接、可恢复。</p>
  <div class="session-layout"><div class="session-column"><h2>Herdr</h2><p>面向 AI Coding Agent 的终端工作区管理器，通过后台 Session Server 持有真实终端进程。</p><ul class="bullet-list"><li>持久化 Session，断开 SSH 后任务仍可继续。</li><li>识别 working、blocked、done 和 idle 状态。</li><li>用 Workspace、Tab 和 Pane 管理多项目与多 Agent。</li><li>支持远程连接、CLI、Socket API 和多 Agent 协作。</li></ul></div><div class="session-column"><h2>Orca</h2><p>面向并行 Coding Agent 的 ADE，将 Agent、Git Worktree、终端、浏览器和代码审查集中到一个工作台。</p><ul class="bullet-list"><li>为不同 Agent 创建隔离 Worktree。</li><li>统一管理 Codex、Claude Code、OpenCode 和 Pi 等终端 Agent。</li><li>支持浏览器选择、Diff 标注和任务交接。</li><li>支持远程与移动协作。</li></ul></div></div>
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
  <h1 class="title">AI Coding 通用工作流</h1>
  <p class="lead">用 Coding Agent 构建软件，核心仍然是目标、架构、Spec 与验证。</p>
  <div class="image-panel workflow-image"><img src="/images/ai-engineering-workflow.png" alt="AI Engineering 工作流总览" /></div>
  <div class="workflow-strip"><div><h3>目标清楚</h3><p>明确范围、验收标准和完成定义。</p></div><div><h3>运行可控</h3><p>配置上下文、权限和工具。</p></div><div><h3>失败可回</h3><p>保留测试、日志、Review 和恢复路径。</p></div></div>
</div>

---

<div class="editorial-slide">
  <h1 class="title">SDD 与 OpenSpec</h1>
  <p class="lead">先用结构化 Spec 明确需求、约束和验收标准，再让 Agent 进入实现。</p>
  <div class="workflow-methods"><div class="method-column"><h2>SDD：规范驱动开发</h2><p>代码是 Spec 的实现结果，Spec 也是后续 Review 和协作的依据。</p><ul class="bullet-list"><li>先澄清需求和边界。</li><li>把验收标准写成可检查的条件。</li><li>让实现、验证和 Review 围绕同一份契约展开。</li></ul></div><div class="method-column"><h2>OpenSpec：设计与变更契约</h2><p>适合沉淀改什么、为什么改、边界和验收标准。</p><div class="method-flow"><span>propose：提出变更</span><span>review / update：评审修改</span><span>apply：开始实现</span><span>archive：归档记录</span></div></div></div>
</div>

---

<div class="editorial-slide">
  <h1 class="title">Superpowers 与 mattpocock</h1>
  <p class="lead">不同方法都在解决同一件事：让 Agent 的执行过程更有纪律。</p>
  <div class="workflow-methods"><div class="method-column"><h2>Superpowers</h2><p>通过 Sub-Agent、TDD、Review 和可选的 Git Worktree，提高交付质量。</p><div class="method-flow"><span>brainstorming：头脑风暴</span><span>plan：编写计划</span><span>execute：执行</span><span>review：审查</span><span>finish：收尾</span></div></div><div class="method-column"><h2>mattpocock/skills</h2><p>用一组 Skills 把需求澄清、Spec、任务拆分、实现和审查串起来。</p><div class="method-flow"><span>grill-with-docs：头脑风暴</span><span>to-spec：生成 Spec</span><span>to-tickets：拆分任务</span><span>implement：实现</span><span>code-review：代码审查</span></div></div></div>
</div>

---

<div class="editorial-slide">
  <h1 class="title">AI 开发工作流的工程化范式</h1>
  <p class="lead">外部工具不会消失，但会逐渐变成可插拔的 Skill、规则和评测层。</p>
  <div class="paradigm-layout"><div class="paradigm-row"><h3>Prompt Engineering</h3><p>把需求说清楚，让模型按预期回答。</p></div><div class="paradigm-row"><h3>Context Engineering</h3><p>让 Agent 看到完成任务所需的信息。</p></div><div class="paradigm-row"><h3>Harness Engineering</h3><p>提供执行环境，让 Agent 调用工具、运行代码并获得反馈。</p></div><div class="paradigm-row"><h3>Loop Engineering</h3><p>让 Agent 自动执行、验证和修正，直到完成或停止。</p></div><div class="paradigm-row"><h3>Graph Engineering</h3><p>让多个各自运行 Loop 的 Agent，按职责、依赖和交接关系协作。</p></div></div>
</div>

---

<div class="editorial-slide chapter-page">
  <div class="chapter-index">第五章</div>
  <div class="chapter-copy">
    <h1>实践与思考</h1>
    <p>把一次成功的协作，沉淀成下一次可以复用的方法。</p>
  </div>
</div>

---

<div class="editorial-slide">
  <h1 class="title">如何写出一个可复用 Skill</h1>
  <p class="lead">好的 Skill 是一类任务的方法包，不是堆满背景知识的长文档。</p>
  <div class="skill-steps"><div class="skill-step"><strong>1</strong><h3>选择真实任务</h3><p>从重复工作中选择一个需求，先让 Agent 完成并得到满意结果。</p></div><div class="skill-step"><strong>2</strong><h3>整理执行经验</h3><p>记录可复用步骤、所需资料、工具和需要反复提醒的要求。</p></div><div class="skill-step"><strong>3</strong><h3>编写 Skill</h3><p>写清操作步骤，整理脚本，附上模板或示例，明确检查和修复方法。</p></div><div class="skill-step"><strong>4</strong><h3>测试效果</h3><p>使用不同任务和模型测试，找到容易失败的环节。</p></div><div class="skill-step"><strong>5</strong><h3>持续改进</h3><p>根据实际使用和分享反馈修改，优先解决共性问题。</p></div></div>
</div>

---

<div class="editorial-slide">
  <h1 class="title">开发者的工作重心</h1>
  <p class="lead">Agent 承担更多执行工作，人仍然需要懂技术、能判断方案，并对交付负责。</p>
  <div class="thought-layout"><div class="thought-column"><h2>从掌勺者到主厨</h2><p>以前更多是自己完成每一道工序，现在更像负责整个厨房：决定做什么，准备环境，安排分工，最后把关出菜质量。</p><ul class="bullet-list"><li>定义目标、范围和优先级。</li><li>准备可执行、可验证的环境。</li><li>审阅变更，判断结果是否达标。</li></ul></div><div class="thought-column"><h2>先对齐，再开火</h2><p>做开发也一样。先和 Agent 说清楚目标、范围、约束和验收标准，不确定的地方通过提问、读代码和讨论逐步对齐。</p><ul class="bullet-list"><li>需求澄清减少返工。</li><li>验证环境形成闭环。</li><li>人从验证者转为审阅者。</li></ul></div></div>
</div>

---

<div class="editorial-slide final">
  <div><h1>从写代码，到设计一个能持续交付的系统</h1><div class="final-line"></div><p>人定义目标，设计环境，把关结果。Agent 承担更多执行，但交付标准仍然需要被人守住。</p><div class="final-conditions"><span>目标清楚</span><span>环境可用</span><span>结果可验</span></div></div>
</div>
