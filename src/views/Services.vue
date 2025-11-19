<template>
  <div class="services">
    <!-- Services Header -->
    <section class="services-header section">
      <div class="container">
        <h2 class="section-title">产品服务</h2>
        <p class="services-intro">
          合末提供全方位的金融服务解决方案，涵盖房地产金融、企业金融等多个领域，
          致力于为客户提供专业、高效、可靠的服务。
        </p>
      </div>
    </section>

    <!-- Real Estate Financial Services -->
    <section class="service-category section bg-light">
      <div class="container">
        <div class="category-header">
          <div class="category-icon">🏠</div>
          <h2>房地产金融服务</h2>
        </div>
        <div class="services-grid">
          <div class="service-detail-card">
            <div class="service-number">01</div>
            <h3>买卖房垫资服务</h3>
            <div class="service-content">
              <h4>服务介绍</h4>
              <p>
                为房产买卖双方提供专业的资金垫付服务，解决交易过程中的资金周转问题。
                我们提供快速、安全、便捷的垫资服务，帮助客户顺利完成房产交易。
              </p>
              <h4>服务特点</h4>
              <ul>
                <li>快速审批，资金及时到位</li>
                <li>专业团队，全程跟踪服务</li>
                <li>安全可靠，多重保障机制</li>
                <li>灵活方案，满足不同需求</li>
              </ul>
              <h4>适用场景</h4>
              <ul>
                <li>房产买卖资金周转</li>
                <li>首付款临时短缺</li>
                <li>尾款支付时间差</li>
                <li>其他房产交易资金需求</li>
              </ul>
            </div>
          </div>
          <div class="service-detail-card">
            <div class="service-number">02</div>
            <h3>银行转贷服务</h3>
            <div class="service-content">
              <h4>服务介绍</h4>
              <p>
                协助企业完成银行贷款转贷业务，优化融资结构，降低融资成本。
                我们提供专业的转贷咨询和办理服务，帮助企业获得更优的融资条件。
              </p>
              <h4>服务特点</h4>
              <ul>
                <li>专业咨询，方案优化</li>
                <li>流程简化，高效办理</li>
                <li>成本降低，利率优化</li>
                <li>全程服务，省心省力</li>
              </ul>
              <h4>适用场景</h4>
              <ul>
                <li>银行贷款到期转贷</li>
                <li>优化融资结构</li>
                <li>降低融资成本</li>
                <li>改善融资条件</li>
              </ul>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- Corporate Financial Services -->
    <section class="service-category section">
      <div class="container">
        <div class="category-header">
          <div class="category-icon">💼</div>
          <h2>企业金融服务</h2>
        </div>
        <div class="services-grid">
          <div class="service-detail-card">
            <div class="service-number">03</div>
            <h3>企业信用过桥</h3>
            <div class="service-content">
              <h4>服务介绍</h4>
              <p>
                为企业提供信用过桥资金支持，帮助企业解决短期资金需求。
                我们提供灵活的资金解决方案，支持企业正常运营和发展。
              </p>
              <h4>服务特点</h4>
              <ul>
                <li>快速放款，及时到位</li>
                <li>信用评估，专业审核</li>
                <li>灵活期限，满足需求</li>
                <li>风险可控，安全可靠</li>
              </ul>
              <h4>适用场景</h4>
              <ul>
                <li>企业短期资金周转</li>
                <li>项目启动资金需求</li>
                <li>应收账款回款前资金需求</li>
                <li>其他临时性资金需求</li>
              </ul>
            </div>
          </div>
          <div class="service-detail-card">
            <div class="service-number">04</div>
            <h3>电商供应链金融</h3>
            <div class="service-content">
              <h4>服务介绍</h4>
              <p>
                为电商企业提供供应链金融服务，支持产业链上下游企业发展。
                我们通过创新的金融产品和服务，助力电商生态健康发展。
              </p>
              <h4>服务特点</h4>
              <ul>
                <li>产业链全覆盖</li>
                <li>数字化风控</li>
                <li>快速响应</li>
                <li>定制化方案</li>
              </ul>
              <h4>适用场景</h4>
              <ul>
                <li>电商平台供应商融资</li>
                <li>供应链资金周转</li>
                <li>订单融资</li>
                <li>库存融资</li>
              </ul>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- CTA Section -->
    <section class="cta-section section bg-light">
      <div class="container">
        <div class="cta-content">
          <h2>需要了解更多？</h2>
          <p>我们的专业团队随时为您提供咨询服务</p>
          <router-link to="/contact" class="btn">立即咨询</router-link>
        </div>
      </div>
    </section>
  </div>
</template>

<script setup>
</script>

<style scoped>
.services {
  flex: 1;
}

.services-intro {
  max-width: 800px;
  margin: 0 auto;
  text-align: center;
  font-size: 1.1rem;
  color: var(--text-light);
  line-height: 1.8;
}

.bg-light {
  background: linear-gradient(180deg, var(--bg-secondary) 0%, var(--bg-primary) 100%);
  position: relative;
}

.bg-light::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background: 
    radial-gradient(circle at 20% 50%, rgba(99, 102, 241, 0.05) 0%, transparent 50%),
    radial-gradient(circle at 80% 80%, rgba(139, 92, 246, 0.05) 0%, transparent 50%);
  pointer-events: none;
}

.category-header {
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 1rem;
  margin-bottom: 3rem;
}

.category-icon {
  font-size: 3.5rem;
  filter: drop-shadow(0 4px 8px rgba(99, 102, 241, 0.2));
}

.category-header h2 {
  font-size: clamp(2rem, 4vw, 3rem);
  background: var(--gradient-primary);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
  margin: 0;
  font-weight: 800;
  letter-spacing: -0.02em;
}

.services-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(500px, 1fr));
  gap: 2rem;
}

.service-detail-card {
  background: var(--bg-primary);
  padding: 2.5rem 2rem;
  border-radius: var(--border-radius-lg);
  box-shadow: var(--shadow-xl);
  position: relative;
  transition: all 0.4s cubic-bezier(0.4, 0, 0.2, 1);
  border: 1px solid var(--border-color);
  overflow: hidden;
}

.service-detail-card::after {
  content: '';
  position: absolute;
  top: -50%;
  right: -50%;
  width: 200%;
  height: 200%;
  background: radial-gradient(circle, rgba(99, 102, 241, 0.1) 0%, transparent 70%);
  opacity: 0;
  transition: opacity 0.4s ease;
}

.service-detail-card:hover::after {
  opacity: 1;
}

.service-detail-card:hover {
  transform: translateY(-12px) scale(1.01);
  box-shadow: var(--shadow-2xl);
  border-color: var(--primary-color);
}

.service-number {
  position: absolute;
  top: -20px;
  left: 30px;
  font-size: 4.5rem;
  font-weight: 900;
  background: var(--gradient-primary);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
  opacity: 0.2;
  line-height: 1;
  letter-spacing: -0.05em;
}

.service-detail-card h3 {
  font-size: clamp(1.5rem, 3vw, 2.25rem);
  background: var(--gradient-primary);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
  margin-bottom: 2rem;
  padding-top: 1rem;
  font-weight: 800;
  letter-spacing: -0.02em;
}

.service-content h4 {
  font-size: 1.4rem;
  color: var(--text-dark);
  margin: 2rem 0 1rem;
  font-weight: 700;
  letter-spacing: -0.01em;
  position: relative;
  padding-left: 1.25rem;
}

.service-content h4::before {
  content: '';
  position: absolute;
  left: 0;
  top: 50%;
  transform: translateY(-50%);
  width: 4px;
  height: 20px;
  background: var(--gradient-primary);
  border-radius: 2px;
}

.service-content h4:first-child {
  margin-top: 0;
}

.service-content p {
  color: var(--text-light);
  line-height: 1.8;
  margin-bottom: 1.5rem;
}

.service-content ul {
  list-style: none;
  padding: 0;
  margin-bottom: 1.5rem;
}

.service-content ul li {
  color: var(--text-light);
  line-height: 1.8;
  padding-left: 1.5rem;
  position: relative;
  margin-bottom: 0.5rem;
}

.service-content ul li::before {
  content: '✓';
  position: absolute;
  left: 0;
  background: var(--gradient-primary);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
  font-weight: 800;
  font-size: 1.1rem;
}

.cta-section {
  text-align: center;
}

.cta-content h2 {
  font-size: clamp(2rem, 4vw, 3rem);
  margin-bottom: 1rem;
  background: var(--gradient-primary);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
  font-weight: 800;
  letter-spacing: -0.02em;
}

.cta-content p {
  font-size: 1.2rem;
  color: var(--text-light);
  margin-bottom: 2rem;
}

@media (max-width: 768px) {
  .services-grid {
    grid-template-columns: 1fr;
  }
  
  .service-detail-card {
    padding: 2rem;
  }
  
  .category-header h2 {
    font-size: 2rem;
  }
  
  .service-detail-card h3 {
    font-size: 1.5rem;
  }
}
</style>

