<template>
  <div class="about">
    <!-- Company Overview -->
    <section class="overview section">
      <div class="container">
        <h2 class="section-title">公司简介</h2>
        <div class="overview-content">
          <div class="overview-text">
            <p class="lead">
              合末成立于2022年，是一家专业的金融服务公司。我们秉承"合抱之木，始于毫末"的理念，
              致力于为企业提供专业、高效、可靠的金融服务解决方案。
            </p>
            <p>
              公司自成立以来，始终坚持以客户为中心，以专业为根本，以创新为动力，在房地产金融、
              企业金融等领域积累了丰富的经验和良好的口碑。
            </p>
          </div>
        </div>
      </div>
    </section>

    <!-- Development History -->
    <section class="history section bg-light">
      <div class="container">
        <h2 class="section-title">发展历程</h2>
        <div class="timeline">
          <div class="timeline-item">
            <div class="timeline-year">2022</div>
            <div class="timeline-content">
              <h3>公司成立</h3>
              <p>合末正式成立，开始为市场提供专业的金融服务</p>
            </div>
          </div>
          <div class="timeline-item">
            <div class="timeline-year">2023</div>
            <div class="timeline-content">
              <h3>业务拓展</h3>
              <p>业务范围不断扩大，服务客户数量持续增长</p>
            </div>
          </div>
          <div class="timeline-item">
            <div class="timeline-year">2024</div>
            <div class="timeline-content">
              <h3>持续发展</h3>
              <p>不断创新服务模式，提升服务质量，成为行业领先企业</p>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- Business Scope -->
    <section class="scope section">
      <div class="container">
        <h2 class="section-title">经营范围</h2>
        <div class="scope-grid">
          <div class="scope-item">
            <div class="scope-icon">🏠</div>
            <h3>房地产金融服务</h3>
            <p>买卖房垫资、银行转贷等房地产相关金融服务</p>
          </div>
          <div class="scope-item">
            <div class="scope-icon">💼</div>
            <h3>企业金融服务</h3>
            <p>企业信用过桥、资金周转等企业金融解决方案</p>
          </div>
          <div class="scope-item">
            <div class="scope-icon">📦</div>
            <h3>供应链金融</h3>
            <p>电商供应链金融、产业链金融服务</p>
          </div>
          <div class="scope-item">
            <div class="scope-icon">🔧</div>
            <h3>金融咨询服务</h3>
            <p>专业的金融咨询和方案设计服务</p>
          </div>
        </div>
      </div>
    </section>

    <!-- Core Products -->
    <section class="products section bg-light">
      <div class="container">
        <h2 class="section-title">主要产品</h2>
        <div class="products-list">
          <div class="product-item">
            <h3>买卖房垫资服务</h3>
            <p>为房产买卖双方提供专业的资金垫付服务，解决交易过程中的资金周转问题</p>
          </div>
          <div class="product-item">
            <h3>银行转贷服务</h3>
            <p>协助企业完成银行贷款转贷业务，优化融资结构，降低融资成本</p>
          </div>
          <div class="product-item">
            <h3>企业信用过桥</h3>
            <p>为企业提供信用过桥资金支持，帮助企业解决短期资金需求</p>
          </div>
          <div class="product-item">
            <h3>电商供应链金融</h3>
            <p>为电商企业提供供应链金融服务，支持产业链上下游企业发展</p>
          </div>
        </div>
      </div>
    </section>

    <!-- Core Competitiveness -->
    <section class="competitiveness section">
      <div class="container">
        <h2 class="section-title">核心竞争力</h2>
        <div class="competitiveness-grid">
          <div class="competitiveness-card">
            <div class="card-number">01</div>
            <h3>专业团队</h3>
            <p>拥有多年金融行业经验的专业团队，深谙市场规律，能够为客户提供精准的金融服务</p>
          </div>
          <div class="competitiveness-card">
            <div class="card-number">02</div>
            <h3>高效服务</h3>
            <p>流程优化，响应迅速，能够在最短时间内完成业务办理，节省客户时间成本</p>
          </div>
          <div class="competitiveness-card">
            <div class="card-number">03</div>
            <h3>风险控制</h3>
            <p>严格的风控体系，多重保障机制，确保资金安全，为客户提供可靠保障</p>
          </div>
          <div class="competitiveness-card">
            <div class="card-number">04</div>
            <h3>创新模式</h3>
            <p>不断创新服务模式，适应市场变化，为客户提供更优质的金融服务体验</p>
          </div>
        </div>
      </div>
    </section>

    <!-- Corporate Culture -->
    <section class="culture section bg-light">
      <div class="container">
        <h2 class="section-title">企业文化</h2>
        <div class="culture-content">
          <p class="culture-intro">
            合末秉承"合抱之木，始于毫末"的企业理念，致力于成为行业领先的金融服务提供商。
            我们相信，只有从细微之处做起，才能成就伟大的事业。
          </p>
          <div class="values-grid">
            <div class="value-card" v-for="value in values" :key="value.id">
              <div class="value-icon">{{ value.icon }}</div>
              <h3>{{ value.title }}</h3>
              <p>{{ value.description }}</p>
            </div>
          </div>
        </div>
      </div>
    </section>
  </div>
</template>

<script setup>
import { ref } from 'vue'

const values = ref([
  {
    id: 1,
    icon: '🤝',
    title: '诚信',
    description: '以诚待人，以信立业，建立长期互信的合作关系'
  },
  {
    id: 2,
    icon: '👥',
    title: '团队',
    description: '团结协作，共同成长，发挥团队最大效能'
  },
  {
    id: 3,
    icon: '💡',
    title: '创新',
    description: '持续创新，追求卓越，引领行业发展'
  },
  {
    id: 4,
    icon: '🔥',
    title: '激情',
    description: '充满激情，积极进取，为客户创造更大价值'
  }
])
</script>

<style scoped>
.about {
  flex: 1;
}

.overview-content {
  max-width: 900px;
  margin: 0 auto;
}

.lead {
  font-size: 1.4rem;
  line-height: 2;
  color: var(--text-dark);
  margin-bottom: 2rem;
  font-weight: 600;
  letter-spacing: -0.01em;
  position: relative;
  padding-left: 1.5rem;
}

.lead::before {
  content: '';
  position: absolute;
  left: 0;
  top: 0;
  bottom: 0;
  width: 4px;
  background: var(--gradient-primary);
  border-radius: 2px;
}

.overview-text p {
  font-size: 1.1rem;
  line-height: 1.8;
  color: var(--text-light);
  margin-bottom: 1rem;
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

.timeline {
  max-width: 800px;
  margin: 0 auto;
  position: relative;
  padding-left: 2rem;
}

.timeline::before {
  content: '';
  position: absolute;
  left: 0;
  top: 0;
  bottom: 0;
  width: 4px;
  background: var(--gradient-primary);
  border-radius: 2px;
}

.timeline-item {
  position: relative;
  margin-bottom: 3rem;
  padding-left: 3rem;
}

.timeline-item::before {
  content: '';
  position: absolute;
  left: -1.75rem;
  top: 0.5rem;
  width: 20px;
  height: 20px;
  background: var(--gradient-primary);
  border-radius: 50%;
  border: 4px solid var(--bg-primary);
  box-shadow: 0 0 0 4px rgba(99, 102, 241, 0.2), var(--shadow-lg);
  z-index: 1;
}

.timeline-year {
  font-size: 1.75rem;
  font-weight: 800;
  background: var(--gradient-primary);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
  margin-bottom: 0.75rem;
  letter-spacing: -0.02em;
}

.timeline-content h3 {
  font-size: 1.5rem;
  margin-bottom: 0.75rem;
  color: var(--text-dark);
  font-weight: 700;
  letter-spacing: -0.01em;
}

.timeline-content p {
  color: var(--text-light);
  line-height: 1.8;
}

.scope-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: 2rem;
}

.scope-item {
  background: var(--bg-primary);
  padding: 2rem 1.5rem;
  border-radius: var(--border-radius-lg);
  text-align: center;
  box-shadow: var(--shadow-lg);
  transition: all 0.4s cubic-bezier(0.4, 0, 0.2, 1);
  border: 1px solid var(--border-color);
  position: relative;
  overflow: hidden;
}

.scope-item::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  height: 4px;
  background: var(--gradient-primary);
  transform: scaleX(0);
  transition: transform 0.4s cubic-bezier(0.4, 0, 0.2, 1);
}

.scope-item:hover::before {
  transform: scaleX(1);
}

.scope-item:hover {
  transform: translateY(-10px);
  box-shadow: var(--shadow-2xl);
  border-color: transparent;
}

.scope-icon {
  font-size: 2.5rem;
  margin-bottom: 1rem;
  filter: drop-shadow(0 4px 8px rgba(99, 102, 241, 0.2));
  transition: transform 0.4s ease;
}

.scope-item:hover .scope-icon {
  transform: scale(1.15) rotate(-5deg);
}

.scope-item h3 {
  font-size: 1.4rem;
  margin-bottom: 0.75rem;
  color: var(--text-dark);
  font-weight: 700;
  letter-spacing: -0.01em;
}

.scope-item p {
  color: var(--text-light);
  line-height: 1.8;
}

.products-list {
  max-width: 900px;
  margin: 0 auto;
}

.product-item {
  background: var(--bg-primary);
  padding: 2rem 1.5rem;
  border-radius: var(--border-radius-lg);
  margin-bottom: 1.5rem;
  box-shadow: var(--shadow-lg);
  transition: all 0.4s cubic-bezier(0.4, 0, 0.2, 1);
  border-left: 4px solid transparent;
  position: relative;
  overflow: hidden;
}

.product-item::before {
  content: '';
  position: absolute;
  left: 0;
  top: 0;
  bottom: 0;
  width: 4px;
  background: var(--gradient-primary);
  transform: scaleY(0);
  transition: transform 0.4s cubic-bezier(0.4, 0, 0.2, 1);
}

.product-item:hover::before {
  transform: scaleY(1);
}

.product-item:hover {
  transform: translateX(15px);
  box-shadow: var(--shadow-2xl);
  border-left-color: var(--primary-color);
}

.product-item h3 {
  font-size: 1.6rem;
  background: var(--gradient-primary);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
  margin-bottom: 0.75rem;
  font-weight: 800;
  letter-spacing: -0.02em;
}

.product-item p {
  color: var(--text-light);
  line-height: 1.8;
}

.competitiveness-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
  gap: 2rem;
}

.competitiveness-card {
  background: var(--bg-primary);
  padding: 2rem 1.5rem;
  border-radius: var(--border-radius-lg);
  box-shadow: var(--shadow-lg);
  position: relative;
  transition: all 0.4s cubic-bezier(0.4, 0, 0.2, 1);
  border: 1px solid var(--border-color);
  overflow: hidden;
}

.competitiveness-card::after {
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

.competitiveness-card:hover::after {
  opacity: 1;
}

.competitiveness-card:hover {
  transform: translateY(-12px) scale(1.02);
  box-shadow: var(--shadow-2xl);
  border-color: var(--primary-color);
}

.card-number {
  position: absolute;
  top: -20px;
  left: 30px;
  font-size: 4rem;
  font-weight: 700;
  color: var(--primary-color);
  opacity: 0.2;
}

.competitiveness-card h3 {
  font-size: 1.6rem;
  margin-bottom: 1.25rem;
  color: var(--text-dark);
  font-weight: 700;
  letter-spacing: -0.01em;
}

.competitiveness-card p {
  color: var(--text-light);
  line-height: 1.8;
}

.culture-content {
  max-width: 1000px;
  margin: 0 auto;
}

.culture-intro {
  font-size: 1.2rem;
  line-height: 1.8;
  text-align: center;
  color: var(--text-light);
  margin-bottom: 3rem;
  max-width: 800px;
  margin-left: auto;
  margin-right: auto;
}

.values-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
  gap: 2rem;
}

.value-card {
  background: var(--bg-primary);
  padding: 2rem 1.5rem;
  border-radius: var(--border-radius-lg);
  text-align: center;
  box-shadow: var(--shadow-lg);
  transition: all 0.4s cubic-bezier(0.4, 0, 0.2, 1);
  border: 1px solid var(--border-color);
  position: relative;
  overflow: hidden;
}

.value-card::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background: var(--gradient-primary);
  opacity: 0;
  transition: opacity 0.4s ease;
  z-index: 0;
}

.value-card:hover::before {
  opacity: 0.05;
}

.value-card:hover {
  transform: translateY(-12px) scale(1.03);
  box-shadow: var(--shadow-2xl);
  border-color: var(--primary-color);
}

.value-card > * {
  position: relative;
  z-index: 1;
}

.value-icon {
  font-size: 2.8rem;
  margin-bottom: 1rem;
  filter: drop-shadow(0 4px 12px rgba(99, 102, 241, 0.25));
  transition: transform 0.4s ease;
}

.value-card:hover .value-icon {
  transform: scale(1.2) rotate(10deg);
}

.value-card h3 {
  font-size: 1.6rem;
  margin-bottom: 1rem;
  background: var(--gradient-primary);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
  font-weight: 800;
  letter-spacing: -0.02em;
}

.value-card p {
  color: var(--text-light);
  line-height: 1.8;
}

@media (max-width: 768px) {
  .timeline {
    padding-left: 1.5rem;
  }
  
  .timeline-item {
    padding-left: 2rem;
  }
  
  .scope-grid,
  .competitiveness-grid,
  .values-grid {
    grid-template-columns: 1fr;
  }
}
</style>

