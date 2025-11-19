<template>
  <div class="home">
    <!-- Banner Section -->
    <section class="hero">
      <div class="hero-content">
        <div class="hero-text">
          <div class="logo-large">
            <div class="logo-icon-large">合</div>
            <h1 class="company-name">合末</h1>
          </div>
          <p class="slogan-large">合抱之木，始于毫末</p>
          <p class="hero-description">专业金融服务，助力企业成长与发展</p>
          <div class="hero-buttons">
            <router-link to="/services" class="btn">了解服务</router-link>
            <router-link to="/contact" class="btn">联系我们</router-link>
          </div>
        </div>
        <div class="hero-image">
          <div class="banner-placeholder">
            <div class="banner-content">
              <h2>专业 · 高效 · 可靠</h2>
              <p>为企业提供全方位的金融解决方案</p>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- Features Section -->
    <section class="features section">
      <div class="container">
        <h2 class="section-title">核心优势</h2>
        <div class="features-grid">
          <div class="feature-card">
            <div class="feature-icon">🏢</div>
            <h3>专业团队</h3>
            <p>拥有丰富的行业经验和专业背景</p>
          </div>
          <div class="feature-card">
            <div class="feature-icon">⚡</div>
            <h3>高效服务</h3>
            <p>快速响应，高效办理，节省您的时间</p>
          </div>
          <div class="feature-card">
            <div class="feature-icon">🔒</div>
            <h3>安全可靠</h3>
            <p>严格风控，保障资金安全</p>
          </div>
          <div class="feature-card">
            <div class="feature-icon">💼</div>
            <h3>多元服务</h3>
            <p>覆盖房地产金融、企业金融等多个领域</p>
          </div>
        </div>
      </div>
    </section>

    <!-- Statistics Section -->
    <section class="statistics section">
      <div class="container">
        <div class="stats-grid">
          <div class="stat-card" v-for="stat in statistics" :key="stat.id">
            <div class="stat-number">{{ stat.number }}</div>
            <div class="stat-label">{{ stat.label }}</div>
            <div class="stat-desc">{{ stat.description }}</div>
          </div>
        </div>
      </div>
    </section>

    <!-- Services Preview -->
    <section class="services-preview section bg-light">
      <div class="container">
        <h2 class="section-title">产品服务</h2>
        <div class="services-grid">
          <div class="service-card" v-for="service in services" :key="service.id">
            <div class="service-icon">{{ service.icon }}</div>
            <h3>{{ service.title }}</h3>
            <p>{{ service.description }}</p>
            <router-link to="/services" class="service-link">了解更多 →</router-link>
          </div>
        </div>
      </div>
    </section>

    <!-- Process Section -->
    <section class="process section">
      <div class="container">
        <h2 class="section-title">服务流程</h2>
        <div class="process-steps">
          <div class="process-step" v-for="(step, index) in processSteps" :key="index">
            <div class="step-number">{{ index + 1 }}</div>
            <div class="step-content">
              <h3>{{ step.title }}</h3>
              <p>{{ step.description }}</p>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- Testimonials Section -->
    <section class="testimonials section bg-light">
      <div class="container">
        <h2 class="section-title">客户评价</h2>
        <div class="testimonials-grid">
          <div class="testimonial-card" v-for="testimonial in testimonials" :key="testimonial.id">
            <div class="testimonial-content">
              <div class="quote-icon">"</div>
              <p>{{ testimonial.content }}</p>
            </div>
            <div class="testimonial-author">
              <div class="author-name">{{ testimonial.name }}</div>
              <div class="author-title">{{ testimonial.title }}</div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- CTA Section -->
    <section class="cta-home section">
      <div class="container">
        <div class="cta-content-home">
          <h2>开启您的金融之旅</h2>
          <p>专业团队随时为您提供咨询服务，助力企业快速发展</p>
          <div class="cta-buttons">
            <router-link to="/contact" class="btn">立即咨询</router-link>
            <router-link to="/services" class="btn btn-outline">查看服务</router-link>
          </div>
        </div>
      </div>
    </section>
  </div>
</template>

<script setup>
import { ref } from 'vue'

const services = ref([
  {
    id: 1,
    icon: '🏠',
    title: '买卖房垫资',
    description: '为房产交易提供专业的资金垫付服务'
  },
  {
    id: 2,
    icon: '🏦',
    title: '银行转贷',
    description: '协助企业完成银行贷款转贷业务'
  },
  {
    id: 3,
    icon: '💳',
    title: '企业信用过桥',
    description: '为企业提供信用过桥资金支持'
  },
  {
    id: 4,
    icon: '📦',
    title: '电商供应链金融',
    description: '为电商企业提供供应链金融服务'
  }
])

const statistics = ref([
  {
    id: 1,
    number: '500+',
    label: '服务客户',
    description: '累计服务企业客户'
  },
  {
    id: 2,
    number: '50亿+',
    label: '业务规模',
    description: '累计业务金额'
  },
  {
    id: 3,
    number: '98%',
    label: '客户满意度',
    description: '客户好评率'
  },
  {
    id: 4,
    number: '24h',
    label: '快速响应',
    description: '平均响应时间'
  }
])

const processSteps = ref([
  {
    title: '需求咨询',
    description: '了解您的具体需求，提供专业咨询服务'
  },
  {
    title: '方案设计',
    description: '根据需求定制专属金融解决方案'
  },
  {
    title: '审核评估',
    description: '专业团队进行风险评估和资质审核'
  },
  {
    title: '资金到位',
    description: '快速审批，资金及时到位'
  },
  {
    title: '持续服务',
    description: '提供全程跟踪和后续服务支持'
  }
])

const testimonials = ref([
  {
    id: 1,
    content: '合末的服务非常专业，帮助我们快速解决了资金周转问题，整个流程高效顺畅，值得信赖。',
    name: '张总',
    title: '某房地产公司 CEO'
  },
  {
    id: 2,
    content: '作为一家成长型企业，我们经常需要资金支持。合末不仅服务专业，而且响应速度非常快，是我们长期合作的伙伴。',
    name: '李总',
    title: '某科技公司 创始人'
  },
  {
    id: 3,
    content: '通过合末的供应链金融服务，我们的业务得到了快速发展，资金链更加稳定，非常感谢他们的专业服务。',
    name: '王总',
    title: '某电商企业 总经理'
  }
])
</script>

<style scoped>
.home {
  flex: 1;
}

.hero {
  background: var(--gradient-primary);
  color: white;
  padding: 80px 0;
  min-height: auto;
  display: flex;
  align-items: center;
  position: relative;
  overflow: hidden;
}

/* 聚光灯效果 */
.hero::before {
  content: '';
  position: absolute;
  top: -50%;
  right: -20%;
  width: 600px;
  height: 600px;
  background: radial-gradient(circle, rgba(255, 255, 255, 0.15) 0%, rgba(255, 255, 255, 0.05) 40%, transparent 70%);
  border-radius: 50%;
  animation: spotlightMove 20s ease-in-out infinite;
  pointer-events: none;
}

.hero::after {
  content: '';
  position: absolute;
  bottom: -30%;
  left: -10%;
  width: 500px;
  height: 500px;
  background: radial-gradient(circle, rgba(255, 255, 255, 0.12) 0%, rgba(255, 255, 255, 0.04) 40%, transparent 70%);
  border-radius: 50%;
  animation: spotlightMove 15s ease-in-out infinite reverse;
  pointer-events: none;
}

@keyframes spotlightMove {
  0%, 100% {
    transform: translate(0, 0) scale(1);
    opacity: 0.6;
  }
  25% {
    transform: translate(50px, -30px) scale(1.1);
    opacity: 0.8;
  }
  50% {
    transform: translate(-30px, 50px) scale(0.9);
    opacity: 0.7;
  }
  75% {
    transform: translate(30px, 30px) scale(1.05);
    opacity: 0.75;
  }
}

@keyframes float {
  0%, 100% { transform: translate(0, 0) scale(1); }
  50% { transform: translate(30px, -30px) scale(1.1); }
}

.hero-content {
  max-width: 1280px;
  margin: 0 auto;
  padding: 0 24px;
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 5rem;
  align-items: center;
  position: relative;
  z-index: 1;
}

.hero-text {
  animation: fadeInLeft 1s ease;
}

.logo-large {
  display: flex;
  align-items: center;
  gap: 1rem;
  margin-bottom: 1.5rem;
}

.logo-icon-large {
  width: 70px;
  height: 70px;
  background: rgba(255, 255, 255, 0.15);
  backdrop-filter: blur(20px) saturate(180%);
  -webkit-backdrop-filter: blur(20px) saturate(180%);
  border-radius: 18px;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 2.2rem;
  font-weight: 800;
  border: 2px solid rgba(255, 255, 255, 0.3);
  box-shadow: 0 8px 32px rgba(0, 0, 0, 0.2), inset 0 1px 0 rgba(255, 255, 255, 0.3);
  position: relative;
  overflow: hidden;
}

.logo-icon-large::before {
  content: '';
  position: absolute;
  top: -50%;
  left: -50%;
  width: 200%;
  height: 200%;
  background: linear-gradient(45deg, transparent, rgba(255, 255, 255, 0.1), transparent);
  animation: shine 3s infinite;
}

@keyframes shine {
  0% { transform: rotate(0deg); }
  100% { transform: rotate(360deg); }
}

.company-name {
  font-size: clamp(2rem, 5vw, 3.5rem);
  font-weight: 900;
  margin: 0;
  letter-spacing: -0.03em;
  text-shadow: 0 4px 20px rgba(0, 0, 0, 0.2);
  background: linear-gradient(135deg, #ffffff 0%, rgba(255, 255, 255, 0.8) 100%);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
}

.slogan-large {
  font-size: 1.4rem;
  font-style: italic;
  margin: 0.75rem 0;
  color: rgba(255, 255, 255, 0.95);
}

.hero-description {
  font-size: 1rem;
  margin: 1rem 0 1.5rem;
  color: rgba(255, 255, 255, 0.9);
  line-height: 1.7;
}

.hero-buttons {
  display: flex;
  gap: 1rem;
  flex-wrap: wrap;
}

.hero-image {
  animation: fadeInRight 1s ease;
}

.banner-placeholder {
  background: rgba(255, 255, 255, 0.12);
  backdrop-filter: blur(30px) saturate(180%);
  -webkit-backdrop-filter: blur(30px) saturate(180%);
  border-radius: 24px;
  padding: 2.5rem;
  text-align: center;
  border: 1px solid rgba(255, 255, 255, 0.25);
  min-height: 280px;
  display: flex;
  align-items: center;
  justify-content: center;
  box-shadow: 0 20px 60px rgba(0, 0, 0, 0.3), inset 0 1px 0 rgba(255, 255, 255, 0.3);
  position: relative;
  overflow: hidden;
}

.banner-placeholder::before {
  content: '';
  position: absolute;
  top: -50%;
  left: -50%;
  width: 200%;
  height: 200%;
  background: radial-gradient(circle, rgba(255, 255, 255, 0.1) 0%, transparent 70%);
  animation: rotate 20s linear infinite;
}

.banner-content {
  position: relative;
  z-index: 1;
}

.banner-content h2 {
  font-size: 2rem;
  margin-bottom: 1rem;
}

.banner-content p {
  font-size: 1.2rem;
  color: rgba(255, 255, 255, 0.9);
}

.features {
  background: var(--bg-primary);
  position: relative;
}

.features-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: 2rem;
}

.feature-card {
  text-align: center;
  padding: 2rem 1.5rem;
  border-radius: var(--border-radius-lg);
  background: var(--bg-primary);
  transition: all 0.4s cubic-bezier(0.4, 0, 0.2, 1);
  border: 1px solid var(--border-color);
  position: relative;
  overflow: hidden;
}

.feature-card::before {
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

.feature-card:hover::before {
  transform: scaleX(1);
}

.feature-card:hover {
  transform: translateY(-10px);
  box-shadow: var(--shadow-2xl);
  border-color: transparent;
}

.feature-icon {
  font-size: 2.5rem;
  margin-bottom: 1rem;
  filter: drop-shadow(0 4px 8px rgba(99, 102, 241, 0.2));
  transition: transform 0.4s ease;
}

.feature-card:hover .feature-icon {
  transform: scale(1.1) rotate(5deg);
}

.feature-card h3 {
  font-size: 1.2rem;
  margin-bottom: 0.5rem;
  color: var(--text-dark);
  font-weight: 700;
  letter-spacing: -0.01em;
}

.feature-card p {
  color: var(--text-light);
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

.services-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
  gap: 2rem;
}

.service-card {
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

.service-card::after {
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

.service-card:hover::after {
  opacity: 1;
}

.service-card:hover {
  transform: translateY(-12px) scale(1.02);
  box-shadow: var(--shadow-2xl);
  border-color: var(--primary-color);
}

.service-icon {
  font-size: 2.8rem;
  margin-bottom: 1rem;
  filter: drop-shadow(0 4px 12px rgba(99, 102, 241, 0.25));
  transition: transform 0.4s ease;
}

.service-card:hover .service-icon {
  transform: scale(1.15) translateY(-5px);
}

.service-card h3 {
  font-size: 1.3rem;
  margin-bottom: 0.75rem;
  color: var(--text-dark);
  font-weight: 700;
  letter-spacing: -0.01em;
}

.service-card p {
  color: var(--text-light);
  margin-bottom: 1.5rem;
  line-height: 1.8;
}

.service-link {
  background: var(--gradient-primary);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
  text-decoration: none;
  font-weight: 600;
  transition: all 0.3s ease;
  display: inline-flex;
  align-items: center;
  gap: 0.5rem;
}

.service-link::after {
  content: '→';
  transition: transform 0.3s ease;
}

.service-link:hover {
  transform: translateX(5px);
}

.service-link:hover::after {
  transform: translateX(5px);
}

/* Statistics Section */
.statistics {
  background: var(--bg-primary);
  position: relative;
}

.statistics::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background: 
    radial-gradient(circle at 30% 50%, rgba(99, 102, 241, 0.03) 0%, transparent 50%),
    radial-gradient(circle at 70% 50%, rgba(139, 92, 246, 0.03) 0%, transparent 50%);
  pointer-events: none;
}

.stats-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: 2rem;
}

.stat-card {
  text-align: center;
  padding: 2rem 1.5rem;
  background: var(--bg-primary);
  border-radius: var(--border-radius-lg);
  border: 1px solid var(--border-color);
  transition: all 0.4s cubic-bezier(0.4, 0, 0.2, 1);
  position: relative;
  overflow: hidden;
}

.stat-card::before {
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

.stat-card:hover::before {
  transform: scaleX(1);
}

.stat-card:hover {
  transform: translateY(-8px);
  box-shadow: var(--shadow-xl);
  border-color: var(--primary-color);
}

.stat-number {
  font-size: 2.5rem;
  font-weight: 900;
  background: var(--gradient-primary);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
  margin-bottom: 0.5rem;
  line-height: 1;
  letter-spacing: -0.03em;
}

.stat-label {
  font-size: 1.1rem;
  font-weight: 700;
  color: var(--text-dark);
  margin-bottom: 0.4rem;
  letter-spacing: -0.01em;
}

.stat-desc {
  font-size: 0.95rem;
  color: var(--text-light);
  line-height: 1.6;
}

/* Process Section */
.process {
  background: var(--bg-primary);
  position: relative;
}

.process-steps {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  gap: 2rem;
  max-width: 1000px;
  margin: 0 auto;
  position: relative;
}

.process-steps::before {
  content: '';
  position: absolute;
  top: 60px;
  left: 0;
  right: 0;
  height: 2px;
  background: linear-gradient(90deg, transparent, var(--primary-color), transparent);
  z-index: 0;
}

.process-step {
  flex: 1;
  min-width: 180px;
  text-align: center;
  position: relative;
  z-index: 1;
}

.step-number {
  width: 80px;
  height: 80px;
  margin: 0 auto 1rem;
  background: var(--gradient-primary);
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 1.8rem;
  font-weight: 900;
  color: white;
  box-shadow: var(--shadow-colored);
  position: relative;
  transition: all 0.4s ease;
}

.process-step:hover .step-number {
  transform: scale(1.1) rotate(5deg);
  box-shadow: 0 25px 50px -12px rgba(99, 102, 241, 0.4);
}

.step-content h3 {
  font-size: 1.1rem;
  font-weight: 700;
  color: var(--text-dark);
  margin-bottom: 0.5rem;
  letter-spacing: -0.01em;
}

.step-content p {
  color: var(--text-light);
  line-height: 1.8;
  font-size: 0.95rem;
}

/* Testimonials Section */
.testimonials-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
  gap: 2rem;
  max-width: 1200px;
  margin: 0 auto;
}

.testimonial-card {
  background: var(--bg-primary);
  padding: 2rem 1.5rem;
  border-radius: var(--border-radius-lg);
  box-shadow: var(--shadow-lg);
  border: 1px solid var(--border-color);
  transition: all 0.4s cubic-bezier(0.4, 0, 0.2, 1);
  position: relative;
  overflow: hidden;
}

.testimonial-card::before {
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

.testimonial-card:hover::before {
  transform: scaleX(1);
}

.testimonial-card:hover {
  transform: translateY(-8px);
  box-shadow: var(--shadow-2xl);
  border-color: var(--primary-color);
}

.quote-icon {
  font-size: 3rem;
  line-height: 1;
  background: var(--gradient-primary);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
  opacity: 0.3;
  margin-bottom: 0.75rem;
  font-family: Georgia, serif;
}

.testimonial-content p {
  color: var(--text-dark);
  line-height: 1.8;
  font-size: 1.05rem;
  margin-bottom: 1.5rem;
  font-style: italic;
}

.testimonial-author {
  border-top: 1px solid var(--border-color);
  padding-top: 1rem;
}

.author-name {
  font-size: 1.1rem;
  font-weight: 700;
  color: var(--text-dark);
  margin-bottom: 0.25rem;
}

.author-title {
  font-size: 0.9rem;
  color: var(--text-light);
}

/* CTA Section */
.cta-home {
  background: var(--gradient-primary);
  color: white;
  position: relative;
  overflow: hidden;
}

/* CTA 聚光灯效果 */
.cta-home::after {
  content: '';
  position: absolute;
  top: -50%;
  left: 50%;
  transform: translateX(-50%);
  width: 600px;
  height: 600px;
  background: radial-gradient(circle, rgba(255, 255, 255, 0.18) 0%, transparent 70%);
  border-radius: 50%;
  animation: spotlightMove 20s ease-in-out infinite;
  pointer-events: none;
}

.cta-home::before {
  content: '';
  position: absolute;
  top: -50%;
  right: -20%;
  width: 600px;
  height: 600px;
  background: radial-gradient(circle, rgba(255, 255, 255, 0.1) 0%, transparent 70%);
  border-radius: 50%;
  animation: float 20s ease-in-out infinite;
}

.cta-content-home {
  text-align: center;
  max-width: 800px;
  margin: 0 auto;
  position: relative;
  z-index: 1;
}

.cta-content-home h2 {
  font-size: clamp(1.75rem, 4vw, 2.5rem);
  font-weight: 900;
  margin-bottom: 0.75rem;
  letter-spacing: -0.02em;
  text-shadow: 0 4px 20px rgba(0, 0, 0, 0.2);
}

.cta-content-home p {
  font-size: 1rem;
  margin-bottom: 1.5rem;
  color: rgba(255, 255, 255, 0.95);
  line-height: 1.7;
}

.cta-buttons {
  display: flex;
  gap: 1rem;
  justify-content: center;
  flex-wrap: wrap;
}

@keyframes fadeInLeft {
  from {
    opacity: 0;
    transform: translateX(-30px);
  }
  to {
    opacity: 1;
    transform: translateX(0);
  }
}

@keyframes fadeInRight {
  from {
    opacity: 0;
    transform: translateX(30px);
  }
  to {
    opacity: 1;
    transform: translateX(0);
  }
}

@media (max-width: 768px) {
  .hero {
    padding: 40px 0;
    min-height: auto;
  }
  
  .hero-content {
    grid-template-columns: 1fr;
    gap: 1.5rem;
    text-align: center;
  }
  
  .company-name {
    font-size: 2rem;
  }
  
  .slogan-large {
    font-size: 1.2rem;
  }
  
  .banner-placeholder {
    min-height: 180px;
    padding: 1.5rem;
  }
  
  .features-grid,
  .services-grid,
  .stats-grid,
  .testimonials-grid {
    grid-template-columns: 1fr;
    gap: 1.5rem;
  }
  
  .process-steps {
    flex-direction: column;
    gap: 1.5rem;
  }
  
  .process-steps::before {
    display: none;
  }
  
  .step-number {
    width: 70px;
    height: 70px;
    font-size: 1.5rem;
  }
  
  .stat-number {
    font-size: 2rem;
  }
  
  .cta-buttons {
    flex-direction: column;
    align-items: center;
    gap: 0.75rem;
  }
  
  .cta-buttons .btn {
    width: 100%;
    max-width: 280px;
    padding: 12px 24px;
  }
}
</style>

