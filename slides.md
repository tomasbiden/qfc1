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
