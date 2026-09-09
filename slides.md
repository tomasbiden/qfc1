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

<div class="project-title-cover">
  <div class="cover-visual" aria-hidden="true">
    <div class="ticket-stack ticket-back"></div>
    <div class="ticket-stack ticket-front">
      <span>SECKILL</span>
      <strong>00:00</strong>
      <i></i>
      <small>LIMITED TICKET</small>
    </div>
    <div class="cover-speed-lines"><i></i><i></i><i></i></div>
  </div>
  <div class="cover-title-copy reveal">
    <img src="/qfc-logo.png" alt="QFC" />
    <span>项目验收答辩</span>
    <h1>门票秒杀系统</h1>
    <p>Ticket Seckill System</p>
  </div>
  <div class="cover-camp-label"><strong>去哪儿门票研发</strong><span>Qunar Ticket</span></div>
  <div class="cover-motto">To be coding，to be working！</div>
</div>

<!--
本次汇报的项目是门票秒杀系统。项目围绕活动配置、库存扣减、订单创建、库存回填和异常兜底，建设一条完整、稳定的秒杀业务链路。
-->

---

<div class="team-intro-page">
  <header class="team-page-title reveal"><span>PROJECT TEAM</span><h1>团队成员</h1></header>
  <div class="team-roster">
    <div class="team-role-row reveal" style="--delay:.05s"><strong>DEV</strong><span>侯双剑</span><span>李柏林</span><span>李淑婷</span></div>
    <div class="team-role-row reveal" style="--delay:.10s"><strong>逆向</strong><span>刘锐</span></div>
    <div class="team-role-row reveal" style="--delay:.15s"><strong>FE</strong><span>秦玉佳</span><span>张雨行</span></div>
    <div class="team-role-row reveal" style="--delay:.20s"><strong>QA</strong><span>肖琼</span></div>
  </div>
  <div class="team-visual reveal" style="--delay:.12s">
    <span>7</span>
    <strong>MEMBERS</strong>
    <p>DEV · 逆向 · FE · QA</p>
    <div class="team-collaboration-line"><i></i><i></i><i></i><i></i></div>
    <small>共同完成门票秒杀系统建设</small>
  </div>
</div>

<!--
项目由七位成员共同完成：DEV 侯双剑、李柏林、李淑婷；逆向刘锐；FE 秦玉佳、张雨行；QA 肖琼。各岗位围绕同一条秒杀业务链路协同建设和验证。
-->

---

<div class="deck-contents-page">
  <div class="contents-sheet reveal">
    <header><span>CONTENTS</span><h1>目录</h1></header>
    <ol>
      <li><b>01</b><strong>需求分析</strong></li>
      <li><b>02</b><strong>系统设计与流程图</strong></li>
      <li><b>03</b><strong>代码讲解</strong></li>
      <li><b>04</b><strong>AI 探索与应用</strong></li>
      <li><b>05</b><strong>项目总结与收获</strong></li>
    </ol>
    <div class="contents-keyboard" aria-hidden="true"><i></i><i></i><i></i><i></i><i></i><i></i></div>
  </div>
</div>

<!--
本次汇报分为五个部分：需求分析、系统设计与流程图、代码讲解、AI 探索与应用，以及项目总结与收获。
-->

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

<div class="topline"><span>2.2 / C端产品详情秒杀流程图</span><span></span></div>

<div class="detail-flow-page">
  <div class="detail-flow-chart reveal">
    <div class="flow-box flow-entry"><strong>APP / RN / H5</strong><span>秒杀详情请求</span></div>
    <i class="flow-down">↓</i>
    <div class="flow-box"><strong>接入与治理层</strong><span>统一http处理入口 | 限流 | 参数解析 | 安全校验 | 反爬</span></div>
    <i class="flow-down">↓</i>
    <div class="flow-box"><strong>路由分发层</strong><span>按 T 值路由到秒杀详情链路</span></div>
    <i class="flow-down">↓</i>
    <div class="flow-box"><strong>业务编排层</strong><span>活动信息解析 | 商品/价格等加载 | 上下文组装 | 页面展示配置加载</span></div>
    <i class="flow-down branch-arrow">↓</i>
    <div class="flow-branches">
      <section><strong>多级缓存层</strong><span>活动缓存<br>商品缓存<br>价格缓存<br>组件数据缓存</span></section>
      <section><strong>并发防护层</strong><span>单Key合并加载<br>超时放行避免阻塞<br>降级兜底<br>防击穿/防放大</span></section>
      <section><strong>页面组装层</strong><span>图片模块<br>榜单模块<br>购买模块<br>卡片聚合输出</span></section>
    </div>
    <i class="flow-down merge-arrow">↓</i>
    <div class="flow-box"><strong>下游能力与第三方依赖层</strong><span>活动后台 | 日历报价 | 产品信息 | 榜单能力 | 图片能力<br>预定须知 | 配置服务/基础公共服务</span></div>
    <i class="flow-down">↓</i>
    <div class="flow-box"><strong>监控与运维保障层</strong><span>总耗时监控 | 成功率/失败率 | 缓存命中/回源信息 | 模块耗时 | 日志埋点</span></div>
    <i class="flow-down">↓</i>
    <div class="flow-box flow-result"><strong>详情页聚合结果</strong><span>返回APP</span></div>
  </div>

  <div class="detail-flow-notes">
    <section class="reveal" style="--delay:.06s"><strong>分域多级缓存：</strong><p>基于Caffeine构建本地多级缓存，按业务域拆分活动、商品、价格等独立缓存实例，差异化配置容量与过期策略，有效承接99%以上的读请求流量，大幅降低下游服务压力。</p></section>
    <section class="reveal" style="--delay:.12s"><strong>异步回源：</strong><p>回源任务提交至独立秒杀缓存线程池，配置严格的超时控制与自动取消机制，避免下游服务慢请求引发线程堆积，从架构层面防止服务雪崩风险。</p></section>
    <section class="reveal" style="--delay:.18s"><strong>击穿防护机制：</strong><p>采用单Key合并加载策略，同热点并发请求仅触发一次回源，从根源抑制流量放大；配合空值缓存策略，有效防御缓存穿透攻击，保障缓存层稳定性。</p></section>
    <section class="reveal" style="--delay:.24s"><strong>全链路模块级埋点：</strong><p>覆盖接口耗时、缓存命中率、请求成功率、回源占比等核心指标，实现从网关到业务层的全链路精细化监控，为性能优化提供数据支撑。</p></section>
  </div>
</div>

---

<div class="topline"><span>2.3 / 压测结果与下游保护</span><span></span></div>

<div class="pressure-test-page">
  <div class="pressure-summary"><strong>一、核心性能表现：</strong><span>4C8G 单机在 300 QPS 下可稳定支撑秒杀详情展示，同时通过本地缓存显著降低下游回源压力。</span></div>

  <table class="pressure-table">
    <thead><tr><th>维度</th><th>结果</th><th>说明</th></tr></thead>
    <tbody>
      <tr><td>单机稳定承载能力</td><td>300 QPS</td><td>满足秒杀活动展示需求</td></tr>
      <tr><td>核心接口耗时</td><td>70ms内</td><td>低延迟、可稳定返回</td></tr>
      <tr><td>压力边界</td><td>400 QPS</td><td>CPU接近85%，耗时明显放大</td></tr>
      <tr><td>下游回源量</td><td>明显低于入口请求量</td><td>本地缓存有效拦截回源压力</td></tr>
    </tbody>
  </table>

  <div class="pressure-analysis">
    <strong>二、性能拐点分析：</strong>
    <ul>
      <li><b>接口耗时图：</b>300 QPS 下接口耗时稳定，满足秒杀活动展示要求；400 QPS 后整体响应时间明显升高，进入单机高负载区间。</li>
      <li><b>CPU 图：</b>随并发提升，CPU 利用率持续升高；当 CPU 接近 85% 时，外围逻辑与线程调度开销被明显放大。</li>
      <li><b>回源量图：</b>入口流量提升后，下游回源量未线性增长；本地缓存有效吸收了大部分重复请求，显著降低了下游压力</li>
    </ul>
  </div>

  <div class="pressure-charts reveal">
    <figure><img src="/img/压测-接口耗时.png" alt="接口耗时图" /><figcaption>接口耗时图</figcaption></figure>
    <figure><img src="/img/压测-CPU.png" alt="CPU 图" /><figcaption>CPU 图</figcaption></figure>
    <figure><img src="/img/压测-回源量.png" alt="回源量图" /><figcaption>回源量图</figcaption></figure>
  </div>

  <div class="pressure-conclusion"><strong>验证结论：</strong><span>方案在单机 300 QPS 下运行稳定，具备上线能力；本地缓存有效降低下游回源压力，兼顾 C 端体验与下游系统保护，后续可通过横向扩容进一步提升承载上限。</span></div>
</div>

---

<div class="topline"><span>2.4 / B 页秒杀下单时序</span><span>完整流程图</span></div>

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

<div class="topline"><span>2.5 / 库存回填流程</span><span>完整流程图</span></div>

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

<div class="chapter-cover">
  <div class="chapter-no reveal">03</div>
  <div class="chapter-copy reveal" style="--delay:.08s">
    <h1>代码讲解</h1>
  </div>
</div>

<!--
第三章进入核心代码讲解。本章沿库存生命周期展开：先讲下单阶段如何安全扣减，再讲失败后如何统一回填。核心关注并发原子性、跨存储一致性和重复执行安全。
-->

---

<div class="topline"><span>3.1 / 代码讲解</span><span>库存扣减总览</span></div>

# 四层防线共同完成一次安全扣减

<div class="deduct-defense-flow">
  <section class="deduct-gate reveal">
    <header><span>01</span><small>FILTER</small></header>
    <strong>前置过滤</strong>
    <p>单机限流<br />活动商品资格<br />Token 消费<br />Redis 库存预检查</p>
    <footer>失败：快速返回</footer>
  </section>
  <i class="deduct-arrow">→</i>
  <section class="deduct-gate reveal" style="--delay:.07s">
    <header><span>02</span><small>SERIALIZE</small></header>
    <strong>用户串行化</strong>
    <p>activityId + userId<br />构造分布式锁<br /><b>获取失败不等待</b></p>
    <footer>失败：请求处理中</footer>
  </section>
  <i class="deduct-arrow">→</i>
  <section class="deduct-gate gate-focus reveal" style="--delay:.14s">
    <header><span>03</span><small>ARBITRATE</small></header>
    <strong>Redis 原子扣减</strong>
    <p>GET 提前预判<br /><b>DECRBY 最终裁决</b><br />负数立即等量回补</p>
    <footer>结果：成功 / 不足</footer>
  </section>
  <i class="deduct-arrow">→</i>
  <section class="deduct-gate gate-final reveal" style="--delay:.21s">
    <header><span>04</span><small>COMMIT</small></header>
    <strong>DB 事务落单</strong>
    <p>条件扣减日历库存<br />写入秒杀订单<br /><b>同事务提交</b></p>
    <footer>异常：回补 Redis</footer>
  </section>
</div>

<div class="deduct-boundary reveal" style="--delay:.28s">
  <div><span>用户锁</span><strong>解决同一用户重复抢</strong><p>同一活动 + 同一用户只允许一个请求进入生单区</p></div>
  <i>≠</i>
  <div><span>原子扣减</span><strong>解决多个用户同时抢</strong><p>所有用户竞争同一库存 Key，由 DECRBY 返回值裁决</p></div>
</div>

<!--
一次安全的库存扣减由四层防线共同完成。前置过滤负责挡住无效请求；活动加用户维度的分布式锁把同一用户的并发请求串行化；Redis DECRBY 裁决多个用户的库存竞争；最终由数据库事务同时完成日历库存扣减和秒杀单入库。用户锁和库存原子扣减解决的是两个不同层次的问题。
-->

---

<div class="topline"><span>3.2 / 代码讲解</span><span>Redis 原子裁决</span></div>

# GET 负责提前失败，DECRBY 完成并发裁决

<div class="deduct-race-layout">
  <section class="deduct-code-panel reveal">
    <header><span>SeckillRedisGateway.deduct()</span><b>库存竞争核心</b></header>
    <div class="deduct-code-body">
      <p class="code-muted">long currentStock = getStock(stockKey);</p>
      <p>if (currentStock &lt; quantity)</p>
      <p class="indent">return INSUFFICIENT;</p>
      <p class="code-focus">Long remaining =</p>
      <p class="indent code-focus">sedis.decrBy(stockKey, quantity);</p>
      <p>if (remaining &gt;= 0)</p>
      <p class="indent code-success">return SUCCESS;</p>
      <p class="code-compensate">returnStock(stockKey, quantity);</p>
      <p>return INSUFFICIENT;</p>
    </div>
  </section>

  <section class="race-board reveal" style="--delay:.10s">
    <header><span>并发演算</span><strong>最后 1 份库存</strong></header>
    <div class="race-scale"><span>读取</span><span>原子扣减</span><span>结果</span><span>处理</span></div>
    <div class="race-row winner">
      <b>请求 A</b><span>GET = 1</span><i>→</i><span>DECRBY = 0</span><i>→</i><strong>成功</strong>
    </div>
    <div class="race-row loser">
      <b>请求 B</b><span>GET = 1</span><i>→</i><span>DECRBY = -1</span><i>→</i><strong>库存不足</strong>
    </div>
    <div class="race-rollback"><span>-1</span><i>INCRBY +1</i><strong>0</strong><p>撤销 B 的无效扣减</p></div>
  </section>
</div>

<div class="deduct-unknown reveal" style="--delay:.18s">
  <span>结果未知</span><strong>DECRBY 抛异常或返回 null</strong><i>→</i><b>STOCK_STATE_UNKNOWN</b><i>→</i><em>禁止盲目 INCRBY</em>
  <p>无法确认命令是否执行时，直接回补可能凭空增加库存</p>
</div>

<div class="deduct-race-conclusion reveal" style="--delay:.24s"><span>判断边界</span><strong>GET 是性能预判，DECRBY 的原子返回值才决定请求是否真正获得库存</strong></div>

<!--
GET 预检查只能帮助库存不足的请求提前失败，不能作为并发正确性的依据。即使请求 A 和 B 都读取到库存为 1，DECRBY 仍会原子执行：A 得到 0 并成功，B 得到负数后立即等量回补并返回库存不足。如果 DECRBY 的结果未知，则不能盲目 INCRBY，否则可能凭空增加库存。
-->

---

<div class="topline"><span>3.3 / 代码讲解</span><span>事务与异常补偿</span></div>

# DB 同事务落单，失败后显式回补 Redis

<div class="deduct-commit-flow reveal">
  <div><span>01</span><strong>Redis 扣减成功</strong><p>库存竞争已经完成</p></div><i>→</i>
  <div><span>02</span><strong>校验有效订单</strong><p>防止用户重复生单</p></div><i>→</i>
  <div><span>03</span><strong>生成秒杀单号</strong><p>构造待落库订单</p></div><i>→</i>
  <div class="commit-transaction"><span>04</span><strong>DB 本地事务</strong><p>扣日历库存 + 写秒杀单</p></div>
</div>

<div class="deduct-transaction-layout">
  <section class="deduct-code-panel compact reveal" style="--delay:.08s">
    <header><span>createAfterStockDeducted()</span><b>事务外补偿</b></header>
    <div class="deduct-code-body">
      <p>try {</p>
      <p class="indent">SeckillOrder active =</p>
      <p class="indent indent-more">selectActiveOrder(...);</p>
      <p class="indent">if (active != null)</p>
      <p class="indent indent-more">throwActiveOrderException(active);</p>
      <p class="indent">long id = generateSeckillId();</p>
      <p class="indent code-focus">return persistenceService.save(...);</p>
      <p>} catch (Exception e) {</p>
      <p class="indent code-compensate">redisGateway.returnStock(</p>
      <p class="indent indent-more code-compensate">key, quantity);</p>
      <p class="indent">throw e;</p>
      <p>}</p>
    </div>
  </section>

  <section class="transaction-box reveal" style="--delay:.14s">
    <header><span>@Transactional</span><strong>同一个 DB 事务</strong></header>
    <div><b>UPDATE</b><p>remaining_stock = remaining_stock - quantity</p><small>WHERE remaining_stock ≥ quantity</small></div>
    <i>+</i>
    <div><b>INSERT</b><p>写入 seckill_order</p><small>记录 Redis / DB 已扣减状态</small></div>
    <footer>任一步失败：两项 DB 修改同时回滚</footer>
  </section>

  <section class="compensation-path reveal" style="--delay:.20s">
    <header>异常出口</header>
    <p>存在有效订单</p>
    <p>单号生成失败</p>
    <p>DB 库存不足</p>
    <p>秒杀单写入失败</p>
    <i>↓</i>
    <strong>Redis INCRBY</strong>
    <small>回补后继续抛出原异常</small>
  </section>
</div>

<div class="deduct-consistency-conclusion reveal" style="--delay:.26s">
  <div><span>DB 内部</span><strong>本地事务保证原子性</strong></div>
  <i>+</i>
  <div><span>Redis ↔ DB</span><strong>显式补偿推动一致性收敛</strong></div>
</div>

<!--
Redis 扣减成功后，系统依次完成有效订单校验、秒杀单号生成和数据库落单。日历库存扣减与秒杀单写入位于同一个本地事务中，任一步失败都会一起回滚。Redis 不在数据库事务内，因此外层 catch 会显式发起 INCRBY 回补，并继续抛出原异常，保留准确的失败语义。
-->

---

<div class="topline"><span>3.4 / 代码讲解</span><span>Redis 统一库存回填</span></div>

# 三类触发场景，共用一套库存回填规则

<div class="stock-return-overview">
  <section class="return-triggers">
    <div class="return-trigger reveal">
      <span>01</span><div><strong>QMQ 订单状态同步</strong><p>异步同步发现订单失败</p></div>
    </div>
    <div class="return-trigger reveal" style="--delay:.06s">
      <span>02</span><div><strong>主站生单失败通知</strong><p>主站明确通知生单失败</p></div>
    </div>
    <div class="return-trigger reveal" style="--delay:.12s">
      <span>03</span><div><strong>QSchedule 定时兜底</strong><p>扫描并补偿长时间未完成订单</p></div>
    </div>
  </section>

  <div class="return-converge reveal" style="--delay:.16s" aria-hidden="true">
    <i></i><i></i><i></i><b>→</b>
  </div>

  <section class="return-service reveal" style="--delay:.20s">
    <small>UNIFIED SERVICE</small>
    <strong>stockReturnService<br />.returnStock(seckillId)</strong>
    <p>调用方只负责判断<strong>何时触发</strong><br />统一服务负责决定<strong>如何回填</strong></p>
  </section>

  <section class="return-responsibilities">
    <div class="return-step reveal" style="--delay:.24s"><span>01</span><strong>读取订单</strong><p>还原回填上下文</p></div>
    <div class="return-step reveal" style="--delay:.29s"><span>02</span><strong>幂等判断</strong><p>已完成则直接返回</p></div>
    <div class="return-step reveal" style="--delay:.34s"><span>03</span><strong>回填库存</strong><p>报价日历 → Redis</p></div>
    <div class="return-step reveal" style="--delay:.39s"><span>04</span><strong>结果收敛</strong><p>状态与返回值明确</p></div>
  </section>
</div>

<div class="return-overview-conclusion reveal" style="--delay:.44s">
  <span>设计价值</span><strong>消除多入口重复实现，所有补偿路径遵守同一套幂等与异常策略</strong>
</div>

<!--
库存回填可能由三个场景触发：QMQ 订单状态同步、主站生单失败通知，以及 QSchedule 定时兜底。三个入口不各自实现库存补偿，而是统一调用 stockReturnService.returnStock。这样，调用方只负责判断何时触发，统一服务集中负责读取订单、幂等判断、报价日历与 Redis 库存回填，以及最终结果收敛。
-->

---

<div class="topline"><span>3.5 / 代码讲解</span><span>幂等与状态收敛</span></div>

# 卫语句 + 状态机，让重复回填可控、异常结果可追踪

<div class="return-code-layout">
  <section class="return-code reveal">
    <header><span>SeckillStockReturnServiceImpl.java</span><b>核心主流程</b></header>
    <div class="return-code-body">
      <p class="code-info">SeckillOrder order = orderMapper.selectBySeckillId(seckillId);</p>
      <p class="code-highlight">if (isStockReturnCompleted(order))</p>
      <p class="code-highlight indent">return StockReturnResult.ALREADY_RETURNED;</p>
      <p>validateStockReturnPreconditions(seckillId, order);</p>
      <p>calendarStockReturnService.returnStock(buildCommand(order));</p>
      <p class="code-highlight">if (!checkRedisStockKeyExists(order))</p>
      <p class="code-highlight indent">return StockReturnResult.DB_RETURNED_REDIS_EXPIRED;</p>
      <p>returnRedisStock(buildCommand(order));</p>
      <p>return StockReturnResult.RETURNED_NOW;</p>
    </div>
  </section>

  <section class="return-code-notes">
    <div class="code-note reveal" style="--delay:.08s"><span>01</span><div><strong>已回填：立即结束</strong><p>卫语句返回 <b>ALREADY_RETURNED</b>，重复消息不会再次增加库存。</p></div></div>
    <div class="code-note reveal" style="--delay:.14s"><span>02</span><div><strong>Redis Key 过期：明确降级</strong><p>数据库库存已回填，不重建过期缓存，返回 <b>DB_RETURNED_REDIS_EXPIRED</b>。</p></div></div>
    <div class="code-note danger reveal" style="--delay:.20s"><span>!</span><div><strong>结果未知：禁止盲目重试</strong><p>Redis 执行结果不确定时抛出明确异常，避免重复 <b>INCRBY</b> 造成超卖。</p></div></div>
  </section>
</div>

<div class="return-state-machine reveal" style="--delay:.26s">
  <div><small>初始状态</small><strong>DEDUCTED</strong><p>库存已扣减</p></div>
  <i>抢占回填权 →</i>
  <div class="state-active"><small>处理中</small><strong>RETURNING</strong><p>CAS + lockVersion</p></div>
  <i>确认回填成功 →</i>
  <div><small>终态</small><strong>RETURNED</strong><p>后续请求直接返回</p></div>
</div>

<div class="return-code-conclusion reveal" style="--delay:.32s">
  <span>核心亮点</span><strong>正常分支用返回值表达，异常分支用错误码暴露；主流程保持线性，库存最多安全回填一次</strong>
</div>

<!--
代码层面有三个关键点。第一，已经完成回填时通过卫语句直接返回 ALREADY_RETURNED，保证重复消息幂等。第二，Redis Key 已过期时只确认数据库库存已回填，不重建缓存，并返回明确的降级结果。第三，Redis 执行结果未知时禁止盲目重试，避免重复 INCRBY。状态上通过 DEDUCTED、RETURNING、RETURNED 三态和 lockVersion 抢占回填权，使库存最多安全回填一次，同时让处理过程可追踪。
-->

---

<div class="topline"><span>4.1 / AI 探索与应用</span><span>复杂代码理解</span></div>

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

<div class="topline"><span>4.2 / AI 探索与应用</span><span>可视化价值</span></div>

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

<div class="topline"><span>4.3 / AI 探索与应用</span><span>传统 AI 编程</span></div>

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

<div class="topline"><span>4.4 / AI 探索与应用</span><span>Loop 编程</span></div>

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

---

<div class="topline"><span>5.1 / 项目总结与收获</span><span>项目成果</span></div>

# 从 0 到 1 建设门票秒杀系统

<div class="project-summary-page">
  <div class="summary-business-chain reveal">
    <div><span>01</span><strong>活动配置</strong></div><i>→</i>
    <div><span>02</span><strong>商品展示</strong></div><i>→</i>
    <div><span>03</span><strong>库存预热</strong></div><i>→</i>
    <div class="chain-highlight"><span>04</span><strong>秒杀抢购</strong></div><i>→</i>
    <div><span>05</span><strong>订单创建</strong></div><i>→</i>
    <div><span>06</span><strong>状态同步</strong></div><i>→</i>
    <div><span>07</span><strong>库存回填</strong></div><i>→</i>
    <div><span>08</span><strong>异常兜底</strong></div>
  </div>

  <div class="summary-capability-grid">
    <section class="summary-capability reveal" style="--delay:.08s">
      <header><span>CONCURRENCY</span><strong>高并发</strong><p>让流量扛得住</p></header>
      <ul>
        <li><b>流量控制</b><span>单机限流 + Redis 总量限流</span></li>
        <li><b>缓存加速</b><span>本地配置 + Caffeine 商品缓存</span></li>
        <li><b>快速失败</b><span>Redis 库存预检查</span></li>
      </ul>
    </section>
    <section class="summary-capability consistency reveal" style="--delay:.14s">
      <header><span>CONSISTENCY</span><strong>一致性</strong><p>让库存最终对得上</p></header>
      <ul>
        <li><b>有序扣减</b><span>Redis 竞争 → DB 扣减</span></li>
        <li><b>失败补偿</b><span>扣减、生单异常及时补偿</span></li>
        <li><b>状态收敛</b><span>订单、Redis、DB 最终一致</span></li>
      </ul>
    </section>
    <section class="summary-capability idempotency reveal" style="--delay:.20s">
      <header><span>IDEMPOTENCY</span><strong>幂等性</strong><p>让重复执行不出错</p></header>
      <ul>
        <li><b>防重复下单</b><span>分布式锁 + 秒杀单校验</span></li>
        <li><b>统一回填</b><span>多入口复用同一库存回填能力</span></li>
        <li><b>防重复回填</b><span>锁 + 状态判断，最多回填一次</span></li>
      </ul>
    </section>
  </div>
</div>

<!--
这个项目完成的不是一个孤立的抢购接口，而是从活动配置、库存预热到订单创建、状态同步、库存回填和异常兜底的完整业务闭环。系统最终围绕三个核心问题形成能力：高并发保证流量扛得住，一致性保证库存最终对得上，幂等性保证重复请求和重复补偿不会造成错误。
-->

---

<div class="topline"><span>5.2 / 项目总结与收获</span><span>个人认知</span></div>

# AI 时代：从执行者走向决策者

<div class="developer-role-page">
  <div class="ai-coverage reveal">
    <div class="coverage-caption"><span>AI 能力边界不断扩大</span><i></i></div>
    <div class="coverage-flow">
      <strong>理解代码</strong><i>→</i><strong>方案设计</strong><i>→</i><strong>编写代码</strong><i>→</i><strong>Code Review</strong><i>→</i><strong>测试验证</strong>
    </div>
  </div>

  <div class="role-shift reveal" style="--delay:.08s">
    <span>执行能力持续增强</span><i>↓</i><strong>开发者价值向决策与责任迁移</strong>
  </div>

  <div class="developer-value-grid">
    <div class="developer-value reveal" style="--delay:.12s"><span>01</span><strong>定义问题</strong><p>明确真正需要解决的问题</p></div>
    <div class="developer-value reveal" style="--delay:.17s"><span>02</span><strong>判断方案</strong><p>权衡收益、成本与潜在风险</p></div>
    <div class="developer-value reveal" style="--delay:.22s"><span>03</span><strong>验证结果</strong><p>区分“能够运行”与“业务正确”</p></div>
    <div class="developer-value final-owner reveal" style="--delay:.27s"><span>04</span><strong>最终负责</strong><p>对设计、质量与生产结果负责</p></div>
  </div>

  <div class="role-conclusion reveal" style="--delay:.32s">
    <span>AI</span><strong>提升执行效率</strong><i>×</i><span>人</span><strong>决定方向与质量</strong>
  </div>
</div>

<!--
AI 的能力正在逐渐覆盖理解、设计、编码、审查和测试等研发环节。当执行能力不断被 AI 增强，开发者的核心价值会更多体现在定义问题、判断方案、验证业务结果以及为最终生产质量负责。AI 提升执行效率，但方向和质量仍然由人决定。
-->

---

<div class="topline"><span>5.3 / 项目总结与收获</span><span>方法沉淀</span></div>

# AI 时代的高质量研发实践

<div class="production-practice-page">
  <div class="production-question reveal"><span>核心问题</span><strong>如何借助 AI 产出生产级代码？</strong></div>

  <div class="production-pipeline">
    <section class="pipeline-stage reveal" style="--delay:.06s">
      <span class="stage-no">01</span><strong>充分理解</strong><b>流程图 / 时序图</b><p>理解业务链路<br />识别异常分支</p>
    </section><i class="pipeline-arrow">→</i>
    <section class="pipeline-stage reveal" style="--delay:.11s">
      <span class="stage-no">02</span><strong>方案设计</strong><b>QSuperpowers</b><p>推演技术方案<br />补齐边界场景</p>
    </section><i class="pipeline-arrow">→</i>
    <section class="pipeline-stage reveal" style="--delay:.16s">
      <span class="stage-no">03</span><strong>风险识别</strong><b>AI Code Review</b><p>审查并发、事务<br />一致性与异常风险</p>
    </section><i class="pipeline-arrow">→</i>
    <section class="pipeline-stage loop-stage reveal" style="--delay:.21s">
      <span class="stage-no">04</span><strong>闭环验证</strong><b>Loop Programming</b><p>Run → Observe<br />Fix → Verify</p>
      <small>从生成走向闭环</small>
    </section><i class="pipeline-arrow">→</i>
    <section class="pipeline-stage owner-stage reveal" style="--delay:.26s">
      <span class="stage-no">05</span><strong>人工兜底</strong><b>Developer Review</b><p>复核技术设计<br />最终质量负责</p>
    </section>
  </div>

  <div class="production-ready reveal" style="--delay:.31s">
    <span>充分理解</span><i>+</i><span>方案推演</span><i>+</i><span>风险审查</span><i>+</i><span>真实验证</span><i>+</i><span>人工把关</span>
    <strong>Production Ready</strong>
  </div>

  <div class="production-conclusion reveal" style="--delay:.36s">
    <span>生产级代码 ≠ AI 生成的代码</span>
    <strong>而是经过完整研发闭环，并由开发者对最终结果负责的代码。</strong>
  </div>
</div>

<!--
高质量 AI 研发不是把需求直接交给 AI 生成代码，而是一条完整的生产流水线：先充分理解业务，再推演方案、识别风险，通过 Loop Programming 接入真实环境反馈，最后由开发者完成关键复核并承担最终责任。只有经过理解、设计、审查、验证和人工把关的代码，才真正具备 Production Ready 的条件。
-->

---

<div class="thanks-page">
  <div class="thanks-pattern" aria-hidden="true">
    <div class="thanks-ticket one"></div>
    <div class="thanks-ticket two"></div>
    <div class="thanks-ticket three"></div>
    <div class="thanks-keyboard"></div>
  </div>
  <div class="thanks-word reveal" aria-label="Thanks">
    <span>T</span><span>h</span><span>a</span><span>n</span><span>k</span><span>s</span>
  </div>
  <div class="thanks-copy reveal" style="--delay:.12s">
    <strong>感谢聆听</strong>
    <span>门票秒杀系统项目组</span>
  </div>
  <div class="thanks-motto">To be coding，to be working！</div>
</div>

<!--
感谢各位的聆听，以上是门票秒杀系统的项目汇报。
-->
