---
theme: default
title: 门票秒杀系统结项答辩
info: 门票秒杀系统结项答辩
author: 门票研发团队
colorSchema: light
aspectRatio: 4/3
canvasWidth: 1440
routerMode: hash
exportFilename: 第一章-需求分析
transition: fade-out
mdc: true
---

<div class="chapter-cover">
  <div class="chapter-no reveal">01</div>
  <div class="chapter-copy reveal" style="--delay:.08s">
    <p class="kicker">TICKET SECKILL</p>
    <h1>需求分析</h1>
  </div>
</div>

<!--
第一章是需求分析，分为项目背景与建设目标、核心业务需求、秒杀场景核心系统需求三个部分。
-->

---

<div class="topline"><span>1.1 / 项目背景与建设目标</span><span>业务目标</span></div>

# 为门票业务提供新的用户增长与营销手段

<div class="growth-loop">
  <div class="growth-core">
    <span>限时 · 限量</span>
    <strong>高吸引力的秒杀营销活动</strong>
    <small>门票业务</small>
  </div>
  <div class="growth-arm arm-acquire reveal">
    <span>01</span><div><strong>拉新</strong><p>通过秒杀活动吸引新用户进入门票业务</p></div>
  </div>
  <div class="growth-arm arm-activate reveal" style="--delay:.08s">
    <span>02</span><div><strong>促活</strong><p>提升老用户的访问频率与活动参与度</p></div>
  </div>
  <div class="growth-arm arm-convert reveal" style="--delay:.16s">
    <span>03</span><div><strong>转化</strong><p>通过秒杀活动引流，进一步带动其他门票商品的交易转化</p></div>
  </div>
  <svg class="growth-path" viewBox="0 0 1400 520" aria-hidden="true">
    <path d="M700 258 C470 258 470 86 290 86" />
    <path d="M700 258 H1110" />
    <path d="M700 258 C470 258 470 430 290 430" />
    <circle cx="700" cy="258" r="8" />
  </svg>
</div>

<!--
通过限时、限量、高吸引力的秒杀营销活动，为门票业务提供新的用户增长与营销手段。

核心目标包括拉新、促活和转化。
-->

---

<div class="topline"><span>1.1 / 项目背景与建设目标</span><span>建设目标</span></div>

# 建设完整的门票秒杀能力

<div class="capability-rail">
  <div class="capability-step reveal">
    <span>01</span><strong>运营活动配置</strong>
  </div>
  <div class="rail-arrow">→</div>
  <div class="capability-step reveal" style="--delay:.06s">
    <span>02</span><strong>秒杀商品展示</strong>
  </div>
  <div class="rail-arrow">→</div>
  <div class="capability-step active reveal" style="--delay:.12s">
    <span>03</span><strong>用户抢购</strong>
  </div>
  <div class="rail-arrow">→</div>
  <div class="capability-step reveal" style="--delay:.18s">
    <span>04</span><strong>订单生成</strong>
  </div>
  <div class="rail-arrow">→</div>
  <div class="capability-step reveal" style="--delay:.24s">
    <span>05</span><strong>订单履约</strong>
  </div>
</div>

<div class="page-conclusion"><strong>建设要求</strong><span>在满足业务需求的同时，保证秒杀场景下系统的稳定性、公平性与交易一致性。</span></div>

<!--
建设完整的门票秒杀能力，覆盖运营活动配置、秒杀商品展示、用户抢购、订单生成和订单履约。

在满足业务需求的同时，保证秒杀场景下系统的稳定性、公平性与交易一致性。
-->

---

<div class="topline"><span>1.2 / 核心业务需求</span><span>运营侧</span></div>

# 运营侧需求

<div class="requirements-list">
  <div class="requirement-row reveal">
    <span>01</span>
    <strong>支持秒杀活动创建、编辑与管理</strong>
  </div>
  <div class="requirement-row reveal" style="--delay:.08s">
    <span>02</span>
    <strong>支持秒杀票种、商品、报价及库存配置</strong>
  </div>
  <div class="requirement-row reveal" style="--delay:.16s">
    <span>03</span>
    <strong>支持秒杀活动生命周期管理</strong>
  </div>
</div>

<!--
运营侧需要支持秒杀活动创建、编辑与管理；支持秒杀票种、商品、报价及库存配置；支持秒杀活动生命周期管理。
-->

---

<div class="topline"><span>1.2 / 核心业务需求</span><span>用户侧</span></div>

# 用户侧需求

<div class="journey-board">
  <div class="journey-phase phase-before">
    <div class="phase-title"><span>活动开始前</span></div>
    <div class="journey-steps">
      <div class="journey-step reveal"><span>01</span><strong>查看秒杀商品</strong></div>
      <i>→</i>
      <div class="journey-step reveal" style="--delay:.06s"><span>02</span><strong>选择商品规格</strong></div>
      <i>→</i>
      <div class="journey-step reveal" style="--delay:.12s"><span>03</span><strong>提前完成游客信息准备</strong></div>
    </div>
  </div>
  <div class="start-marker"><strong>活动开始</strong></div>
  <div class="journey-phase phase-after">
    <div class="phase-title"><span>活动开始后</span></div>
    <div class="journey-steps after-steps">
      <div class="journey-step reveal" style="--delay:.18s"><span>04</span><strong>参与抢购</strong></div>
      <i>→</i>
      <div class="journey-step reveal" style="--delay:.24s"><span>05</span><strong>确认订单</strong></div>
      <i>→</i>
      <div class="journey-step reveal" style="--delay:.30s"><span>06</span><strong>完成支付</strong></div>
    </div>
  </div>
</div>

<div class="page-conclusion"><strong>用户侧目标</strong><span>提供完整的秒杀购票体验。</span></div>

<!--
活动开始前，用户可以查看秒杀商品、选择商品规格、提前完成游客信息准备。

活动开始后，用户参与抢购、确认订单并完成支付。提供完整的秒杀购票体验。
-->

---

<div class="topline"><span>1.3 / 秒杀场景核心系统需求</span><span>系统要求</span></div>

# 秒杀场景核心系统需求

<div class="system-requirements">
  <div class="system-requirement reveal">
    <span>01</span><div><strong>高并发下的系统稳定性</strong><p>瞬时高并发 → 避免流量洪峰直接冲击核心交易链路</p></div>
  </div>
  <div class="system-requirement reveal" style="--delay:.06s">
    <span>02</span><div><strong>库存准确性</strong><p>有限库存 + 并发抢购 → 防止超卖，同时避免异常导致少卖</p></div>
  </div>
  <div class="system-requirement reveal" style="--delay:.12s">
    <span>03</span><div><strong>秒杀链路防绕过</strong><p>秒杀商品必须通过秒杀链路完成资格及库存校验，防止绕过秒杀流程直接生单。</p></div>
  </div>
  <div class="system-requirement reveal" style="--delay:.18s">
    <span>04</span><div><strong>性能要求</strong><p>秒杀核心链路尽量减少对下游系统的实时依赖，降低抢购链路耗时</p></div>
  </div>
</div>

<!--
秒杀场景的核心系统需求包括高并发下的系统稳定性、库存准确性、秒杀链路防绕过和性能要求。
-->

---

<div class="topline"><span>1.3 / 秒杀场景核心系统需求</span><span>原有交易链路</span></div>

# 最小化对原有交易链路的影响

<div class="requirements-list compact-list">
  <div class="requirement-row reveal"><span>01</span><strong>秒杀能力在现有门票交易体系上扩展</strong></div>
  <div class="requirement-row reveal" style="--delay:.06s"><span>02</span><strong>普通商品继续使用原有购票流程</strong></div>
  <div class="requirement-row reveal" style="--delay:.12s"><span>03</span><strong>秒杀逻辑仅针对秒杀商品生效</strong></div>
  <div class="requirement-row reveal" style="--delay:.18s"><span>04</span><strong>避免秒杀流量及秒杀逻辑影响普通门票业务</strong></div>
</div>

<!--
秒杀能力在现有门票交易体系上扩展；普通商品继续使用原有购票流程；秒杀逻辑仅针对秒杀商品生效；避免秒杀流量及秒杀逻辑影响普通门票业务。
-->

---

<div class="chapter-cover">
  <div class="chapter-no reveal">02</div>
  <div class="chapter-copy reveal" style="--delay:.08s">
    <h1>系统设计与流程图</h1>
  </div>
</div>

<!--
第二章进入系统设计与流程图，首先介绍秒杀系统的库表设计。
-->

---

<div class="topline"><span>2.1 / 库表设计</span><span>配置域 ER 图</span></div>

# 秒杀核心库表及逻辑关联

<div class="er-board">
  <svg class="er-links" viewBox="0 0 1244 650" aria-hidden="true">
    <path d="M280 160 H321" />
    <path d="M601 160 H642" />
    <path d="M902 160 H934" />
    <path d="M140 290 V315 H180 V340" />
    <path d="M140 290 V315 H850 V325" />
    <path class="logical-match" d="M1089 310 H1125 V465 H1100" />
    <text x="284" y="146">1:N</text>
    <text x="605" y="146">1:N</text>
    <text x="905" y="146">1:N</text>
    <text x="151" y="309">1:N</text>
    <text x="500" y="302">1:N</text>
    <text x="1137" y="395">字段匹配</text>
  </svg>

  <section class="er-entity er-activity reveal">
    <header><strong>seckill_activity</strong><span>秒杀活动主表</span></header>
    <p><b>PK</b> id　<b>UK</b> activity_code</p>
    <p>status / purchase_limit</p>
    <p>start_time / end_time</p>
  </section>

  <section class="er-entity er-spu reveal" style="--delay:.04s">
    <header><strong>seckill_activity_spu</strong><span>活动票种配置</span></header>
    <p><b>PK</b> id</p>
    <p>activity_id</p>
    <p>first_lv_ticket_type_id</p>
    <p>second_lv_ticket_type_id</p>
  </section>

  <section class="er-entity er-sku reveal" style="--delay:.08s">
    <header><strong>seckill_activity_sku</strong><span>活动产品</span></header>
    <p><b>PK</b> id</p>
    <p>activity_id / activity_spu_id</p>
    <p>product_id / spec_values</p>
  </section>

  <section class="er-entity er-calendar reveal" style="--delay:.12s">
    <header><strong>seckill_sku_calendar</strong><span>商品报价日历</span></header>
    <p><b>PK</b> id</p>
    <p>activity_id / activity_sku_id</p>
    <p>product_id / price_id / use_date</p>
    <p>configured_stock / remaining_stock</p>
  </section>

  <section class="er-entity er-log reveal" style="--delay:.16s">
    <header><strong>seckill_operation_log</strong><span>配置操作日志</span></header>
    <p><b>PK</b> id</p>
    <p>activity_id</p>
    <p>operation_type / operator_name</p>
    <p>change_content</p>
  </section>

  <section class="er-entity er-order reveal" style="--delay:.20s">
    <header><strong>seckill_order</strong><span>秒杀订单</span></header>
    <p><b>PK</b> id　<b>UK</b> seckill_id / display_id</p>
    <p>seckill_activity_id</p>
    <p>product_id / price_id / use_date</p>
    <p>redis_stock_status / calendar_stock_status</p>
  </section>

  <div class="er-legend"><span>实线：字段逻辑关联</span><span class="dashed">虚线：订单与报价库存字段匹配</span><span>DDL 无物理外键</span></div>
</div>

<!--
库表之间未声明物理外键，图中的连线只表示代码和字段层面的逻辑关联。
-->

---

<div class="topline"><span>2.2 / B 页秒杀下单时序</span><span>完整流程图</span></div>

# B 页秒杀下单时序图

<a class="diagram-url reveal" href="/img/B页秒杀下单时序图.png" target="_blank" rel="noopener noreferrer">
  <span>查看完整原图</span>
  <strong>/img/B页秒杀下单时序图.png</strong>
  <i>↗</i>
</a>

<!--
点击页面中的链接，在新窗口查看完整的 B 页秒杀下单时序图。
-->

---

<div class="topline"><span>2.3 / 库存回填流程</span><span>完整流程图</span></div>

# 库存回填流程图

<a class="diagram-url reveal" href="/img/库存回填流程图.png" target="_blank" rel="noopener noreferrer">
  <span>查看完整原图</span>
  <strong>/img/库存回填流程图.png</strong>
  <i>↗</i>
</a>

<!--
点击页面中的链接，在新窗口查看完整的库存回填流程图。
-->

---

<div class="topline"><span>3.1 / AI 探索与应用</span><span>复杂代码理解</span></div>

# AI 辅助复杂代码理解

<div class="ai-understanding">
  <div class="ai-pain-grid">
    <div class="ai-pain reveal">
      <span>01</span>
      <strong>调用链长</strong>
      <p>频繁跨类、跨模块跳转</p>
    </div>
    <div class="ai-pain reveal" style="--delay:.06s">
      <span>02</span>
      <strong>分支复杂</strong>
      <p>正常、异常、兜底逻辑交织</p>
    </div>
    <div class="ai-pain reveal" style="--delay:.12s">
      <span>03</span>
      <strong>全局视角弱</strong>
      <p>容易陷入局部实现</p>
    </div>
  </div>

  <div class="ai-code-flow reveal" style="--delay:.18s">
    <div class="ai-flow-node source"><span>输入</span><strong>源码</strong></div>
    <i>→</i>
    <div class="ai-flow-node"><span>识别</span><strong>调用关系</strong></div>
    <i>→</i>
    <div class="ai-flow-node"><span>提取</span><strong>业务节点</strong></div>
    <i>→</i>
    <div class="ai-flow-node"><span>梳理</span><strong>条件与异常</strong></div>
    <i>→</i>
    <div class="ai-flow-node"><span>生成</span><strong>流程图 / 时序图</strong></div>
    <i>→</i>
    <div class="ai-flow-node model"><span>输出</span><strong>整体业务模型</strong></div>
  </div>

  <div class="ai-core-thought reveal" style="--delay:.24s">
    <span>核心思想</span>
    <strong>将非结构化的代码阅读过程，转化为结构化、可视化的业务理解过程。</strong>
  </div>
</div>

<!--
随着系统规模增长，业务逻辑会分散在多个模块、类和方法中。传统阅读方式需要频繁跳转，正常、异常和兜底分支又相互交织，很容易陷入局部实现。AI 可以从源码中识别调用关系、提取业务节点并梳理条件分支，最终形成流程图和时序图，帮助开发人员建立整体业务模型。
-->

---

<div class="topline"><span>3.2 / AI 探索与应用</span><span>可视化价值</span></div>

# AI + 可视化降低复杂系统理解成本

<div class="ai-visual-value">
  <div class="ai-diagram-panel flow-panel reveal">
    <header><span>业务视角</span><strong>流程图</strong><small>关注“业务怎么走”</small></header>
    <div class="mini-flow">
      <b>输入</b><i>→</i><b>校验</b><i>→</i><b>处理</b><i>→</i><b>分支</b><i>→</i><b>结果</b>
    </div>
    <p>适合业务流程、条件判断与异常路径分析</p>
  </div>

  <div class="ai-diagram-panel sequence-panel reveal" style="--delay:.08s">
    <header><span>协作视角</span><strong>时序图</strong><small>关注“系统怎么协作”</small></header>
    <div class="mini-sequence">
      <div><b>用户</b><span></span></div>
      <i>→</i>
      <div><b>服务 A</b><span></span></div>
      <i>→</i>
      <div><b>服务 B</b><span></span></div>
      <i>→</i>
      <div><b>中间件</b><span></span></div>
      <i>→</i>
      <div><b>服务 C</b><span></span></div>
    </div>
    <p>适合跨服务调用、先后顺序与异常时序分析</p>
  </div>

  <div class="human-ai-handoff reveal" style="--delay:.16s">
    <div class="role-block ai-role"><span>AI</span><strong>提取 · 归纳 · 可视化</strong></div>
    <div class="handoff-arrow"><span>信息模型</span><i>→</i></div>
    <div class="role-block human-role"><span>开发人员</span><strong>校验 · 判断 · 设计</strong></div>
  </div>

  <div class="ai-value-chain reveal" style="--delay:.24s">
    <strong>更快建立全局视角</strong><i>→</i><strong>更容易发现关键分支</strong><i>→</i><strong>降低复杂系统理解成本</strong>
  </div>
</div>

<!--
流程图关注业务如何流转，适合分析输入、校验、处理、分支和结果；时序图关注系统如何协作，适合分析跨服务调用顺序和异常时序。AI 负责提取、归纳和可视化，开发人员负责结合源码完成校验、判断和设计。AI 提升的是信息整理与认知效率，关键业务判断仍由开发人员完成。
-->

---

<div class="topline"><span>3.3 / AI 探索与应用</span><span>传统 AI 编程</span></div>

# AI 会“写代码”，但不一定真正“完成开发”

<div class="traditional-ai-page">
  <div class="traditional-chain reveal">
    <div class="chain-node"><span>需求</span></div><i>→</i>
    <div class="chain-node ai-code"><span>AI 编码</span></div><i>→</i>
    <div class="chain-node manual"><small>人工</small><span>Review</span></div><i>→</i>
    <div class="chain-node manual"><small>人工</small><span>运行</span></div><i>→</i>
    <div class="chain-node manual"><small>人工</small><span>测试</span></div><i>→</i>
    <div class="chain-node issue"><span>发现问题</span></div><i>→</i>
    <div class="chain-node ai-code"><span>再交给 AI</span></div>
  </div>

  <div class="manual-handoff reveal" style="--delay:.08s">
    <span>编码与验证之间存在多次人工接力</span>
  </div>

  <div class="traditional-limit-grid">
    <div class="traditional-limit reveal" style="--delay:.12s">
      <span>01</span><strong>缺少运行环境</strong><p>AI 只能基于静态代码推理</p>
    </div>
    <div class="traditional-limit reveal" style="--delay:.18s">
      <span>02</span><strong>缺少运行反馈</strong><p>无法获得真实日志、异常与数据状态</p>
    </div>
    <div class="traditional-limit reveal" style="--delay:.24s">
      <span>03</span><strong>验证依赖人工</strong><p>编码与测试仍需人工反复衔接</p>
    </div>
  </div>

  <div class="development-thesis reveal" style="--delay:.30s">
    <span>开发闭环</span>
    <strong>代码生成只是起点；能够运行、观察、验证和修正，才是完整的软件开发过程。</strong>
  </div>
</div>

<!--
传统 AI 编程通常止步于代码生成。AI 输出代码后，仍需要开发人员完成 Review、运行和测试，再把发现的问题重新交给 AI。由于 AI 缺少真实运行环境和运行反馈，编码与验证之间存在多次人工接力，尚未形成完整的软件开发闭环。
-->

---

<div class="topline"><span>3.4 / AI 探索与应用</span><span>Loop 编程</span></div>

# Loop 编程：构建 AI 自主验证闭环

<div class="loop-programming-page">
  <div class="loop-cycle reveal">
    <svg viewBox="0 0 760 520" aria-hidden="true">
      <defs>
        <marker id="loop-arrow" markerWidth="10" markerHeight="10" refX="8" refY="3" orient="auto">
          <path d="M0,0 L0,6 L9,3 z"></path>
        </marker>
      </defs>
      <path d="M205 90 H300"></path>
      <path d="M460 90 H555"></path>
      <path d="M650 145 V330"></path>
      <path d="M555 410 H460"></path>
      <path d="M300 410 H205"></path>
      <path d="M110 330 V145"></path>
    </svg>
    <div class="loop-node loop-read"><span>Read</span><strong>理解代码</strong></div>
    <div class="loop-node loop-code"><span>Code</span><strong>编写 / 修改</strong></div>
    <div class="loop-node loop-run"><span>Run</span><strong>启动环境</strong></div>
    <div class="loop-node loop-observe"><span>Observe</span><strong>日志 / 状态</strong></div>
    <div class="loop-node loop-fix"><span>Fix</span><strong>定位并修复</strong></div>
    <div class="loop-node loop-verify"><span>Verify</span><strong>执行测试</strong></div>
    <div class="loop-feedback"><span>真实反馈</span><strong>可执行<br />可观察<br />可验证</strong></div>
  </div>

  <div class="agent-evolution reveal" style="--delay:.12s">
    <span class="evolution-label">能力跃迁</span>
    <div class="evolution-from"><small>传统 AI</small><strong>Code Generator</strong><p>根据上下文生成代码</p></div>
    <i>↓</i>
    <div class="evolution-to"><small>Loop 编程</small><strong>开发 Agent</strong><p>理解代码 + 执行代码<br />获取反馈 + 自我修正<br />验证结果</p></div>
  </div>

  <div class="loop-conclusion reveal" style="--delay:.22s">
    <span>核心</span>
    <strong>不是让 AI 写更多代码，而是为 AI 建立“可执行、可观察、可验证”的反馈环境。</strong>
  </div>
</div>

<!--
Loop 编程为 AI 提供真实的执行和反馈环境，使它能够完成理解代码、编写修改、启动环境、执行测试、观察日志与状态、定位问题、修复并重新验证的循环。核心不是让 AI 写更多代码，而是让 AI 从 Code Generator 转变为具备自主验证能力的开发 Agent。
-->
