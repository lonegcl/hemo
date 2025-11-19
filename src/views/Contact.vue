<template>
  <div class="contact">
    <!-- Hero Section -->
    <section class="contact-hero section">
      <div class="container">
        <div class="hero-content">
          <h1 class="hero-title">联系我们</h1>
          <p class="hero-subtitle">我们期待与您建立合作关系，如有任何问题或需求，欢迎随时与我们联系</p>
        </div>
      </div>
    </section>

    <!-- Main Contact Section -->
    <section class="main-contact section">
      <div class="container">
        <div class="contact-layout">
          <!-- Left: Contact Info -->
          <div class="contact-info-panel">
            <div class="info-card">
              <div class="info-item">
                <div class="info-icon-wrapper">
                  <div class="info-icon">📍</div>
                </div>
                <div class="info-content">
                  <h3>公司地址</h3>
                  <p>上海市浦东新区XX路XX号XX大厦XX层</p>
                  <span class="info-note">（具体地址请根据实际情况填写）</span>
                </div>
              </div>

              <div class="info-item">
                <div class="info-icon-wrapper">
                  <div class="info-icon">🕐</div>
                </div>
                <div class="info-content">
                  <h3>工作时间</h3>
                  <p>周一至周五：<strong>9:00 - 18:00</strong></p>
                  <p>周六：<strong>9:00 - 12:00</strong></p>
                  <p>周日及法定节假日：休息</p>
                </div>
              </div>

              <div class="info-item">
                <div class="info-icon-wrapper">
                  <div class="info-icon">📞</div>
                </div>
                <div class="info-content">
                  <h3>联系电话</h3>
                  <a href="tel:400-XXX-XXXX" class="contact-link">400-XXX-XXXX</a>
                  <a href="tel:021-XXXX-XXXX" class="contact-link">021-XXXX-XXXX</a>
                  <span class="info-note">（请根据实际情况填写）</span>
                </div>
              </div>

              <div class="info-item">
                <div class="info-icon-wrapper">
                  <div class="info-icon">✉️</div>
                </div>
                <div class="info-content">
                  <h3>企业邮箱</h3>
                  <a href="mailto:info@hemo.com" class="contact-link">info@hemo.com</a>
                  <a href="mailto:business@hemo.com" class="contact-link">business@hemo.com</a>
                  <span class="info-note">（请根据实际情况填写）</span>
                </div>
              </div>
            </div>
          </div>

          <!-- Right: Map -->
          <div class="map-panel">
            <div class="map-card">
              <h3 class="map-title">公司位置</h3>
              <div class="map-container">
                <div class="map-placeholder">
                  <div class="map-icon">🗺️</div>
                  <p>地图位置</p>
                  <span class="map-note">（可集成百度地图或高德地图）</span>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- Social Media Section -->
    <section class="social-section section bg-light">
      <div class="container">
        <h2 class="section-title">关注我们</h2>
        <div class="social-grid">
          <div class="social-card">
            <div class="social-icon-wrapper">
              <div class="social-icon">📱</div>
            </div>
            <div class="qr-code-placeholder">
              <div class="qr-icon">📱</div>
              <p>公众号二维码</p>
            </div>
            <h3>微信公众号</h3>
            <p>扫描二维码关注我们，获取最新资讯</p>
          </div>

          <div class="social-card">
            <div class="social-icon-wrapper">
              <div class="social-icon">🎵</div>
            </div>
            <div class="qr-code-placeholder">
              <div class="qr-icon">🎵</div>
              <p>抖音二维码</p>
            </div>
            <h3>抖音账号</h3>
            <p>关注我们的抖音账号，了解更多内容</p>
          </div>
        </div>
      </div>
    </section>
  </div>
</template>

<script setup>
</script>

<style scoped>
.contact {
  flex: 1;
}

/* Hero Section */
.contact-hero {
  background: var(--gradient-primary);
  color: white;
  padding: 60px 0;
  text-align: center;
  position: relative;
  overflow: hidden;
}

/* 聚光灯效果 */
.contact-hero::before {
  content: '';
  position: absolute;
  top: -50%;
  left: 50%;
  transform: translateX(-50%);
  width: 500px;
  height: 500px;
  background: radial-gradient(circle, rgba(255, 255, 255, 0.15) 0%, transparent 70%);
  border-radius: 50%;
  animation: spotlightMove 18s ease-in-out infinite;
  pointer-events: none;
}

@keyframes spotlightMove {
  0%, 100% {
    transform: translateX(-50%) translate(0, 0) scale(1);
    opacity: 0.6;
  }
  25% {
    transform: translateX(-50%) translate(50px, -30px) scale(1.1);
    opacity: 0.8;
  }
  50% {
    transform: translateX(-50%) translate(-30px, 50px) scale(0.9);
    opacity: 0.7;
  }
  75% {
    transform: translateX(-50%) translate(30px, 30px) scale(1.05);
    opacity: 0.75;
  }
}

.hero-content {
  max-width: 800px;
  margin: 0 auto;
}

.hero-title {
  font-size: clamp(2rem, 5vw, 3rem);
  font-weight: 900;
  margin-bottom: 1rem;
  letter-spacing: -0.02em;
  text-shadow: 0 4px 20px rgba(0, 0, 0, 0.2);
}

.hero-subtitle {
  font-size: 1.1rem;
  color: rgba(255, 255, 255, 0.95);
  line-height: 1.8;
}

/* Main Contact Layout */
.main-contact {
  background: var(--bg-primary);
}

.contact-layout {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 3rem;
  max-width: 1200px;
  margin: 0 auto;
}

/* Contact Info Panel */
.contact-info-panel {
  display: flex;
  flex-direction: column;
}

.info-card {
  background: var(--bg-primary);
  border-radius: var(--border-radius-xl);
  padding: 2.5rem;
  box-shadow: var(--shadow-xl);
  border: 1px solid var(--border-color);
}

.info-item {
  display: flex;
  gap: 1.5rem;
  padding: 1.5rem 0;
  border-bottom: 1px solid var(--border-color);
  transition: all 0.3s ease;
}

.info-item:last-child {
  border-bottom: none;
}

.info-item:hover {
  padding-left: 0.5rem;
}

.info-icon-wrapper {
  flex-shrink: 0;
  width: 60px;
  height: 60px;
  display: flex;
  align-items: center;
  justify-content: center;
  background: linear-gradient(135deg, rgba(99, 102, 241, 0.1) 0%, rgba(139, 92, 246, 0.1) 100%);
  border-radius: 12px;
  transition: all 0.3s ease;
}

.info-item:hover .info-icon-wrapper {
  background: var(--gradient-primary);
  transform: scale(1.1) rotate(5deg);
}

.info-icon {
  font-size: 1.8rem;
  filter: drop-shadow(0 2px 4px rgba(99, 102, 241, 0.2));
}

.info-item:hover .info-icon {
  filter: drop-shadow(0 4px 8px rgba(99, 102, 241, 0.4));
}

.info-content {
  flex: 1;
}

.info-content h3 {
  font-size: 1.2rem;
  font-weight: 700;
  color: var(--text-dark);
  margin-bottom: 0.75rem;
  letter-spacing: -0.01em;
}

.info-content p {
  color: var(--text-light);
  line-height: 1.8;
  margin-bottom: 0.5rem;
  font-size: 0.95rem;
}

.info-content p strong {
  color: var(--text-dark);
  font-weight: 600;
}

.contact-link {
  display: block;
  background: var(--gradient-primary);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
  font-weight: 600;
  font-size: 1.1rem;
  text-decoration: none;
  margin-bottom: 0.5rem;
  transition: all 0.3s ease;
}

.contact-link:hover {
  transform: translateX(5px);
  opacity: 0.8;
}

.info-note {
  display: block;
  font-size: 0.85rem;
  color: #9ca3af;
  font-style: italic;
  margin-top: 0.5rem;
}

/* Map Panel */
.map-panel {
  display: flex;
  flex-direction: column;
}

.map-card {
  background: var(--bg-primary);
  border-radius: var(--border-radius-xl);
  padding: 2.5rem;
  box-shadow: var(--shadow-xl);
  border: 1px solid var(--border-color);
  height: 100%;
  display: flex;
  flex-direction: column;
}

.map-title {
  font-size: 1.3rem;
  font-weight: 700;
  color: var(--text-dark);
  margin-bottom: 1.5rem;
  letter-spacing: -0.01em;
  background: var(--gradient-primary);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
}

.map-container {
  flex: 1;
  border-radius: var(--border-radius-lg);
  overflow: hidden;
}

.map-placeholder {
  background: linear-gradient(135deg, rgba(99, 102, 241, 0.05) 0%, rgba(139, 92, 246, 0.05) 100%);
  height: 100%;
  min-height: 400px;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  border: 2px dashed var(--border-color);
  transition: all 0.3s ease;
}

.map-placeholder:hover {
  border-color: var(--primary-color);
  background: linear-gradient(135deg, rgba(99, 102, 241, 0.1) 0%, rgba(139, 92, 246, 0.1) 100%);
}

.map-icon {
  font-size: 3rem;
  margin-bottom: 1rem;
  filter: drop-shadow(0 4px 12px rgba(99, 102, 241, 0.25));
  transition: transform 0.3s ease;
}

.map-placeholder:hover .map-icon {
  transform: scale(1.1) rotate(-5deg);
}

.map-placeholder p {
  font-size: 1.1rem;
  color: var(--text-dark);
  margin-bottom: 0.5rem;
  font-weight: 500;
}

.map-note {
  font-size: 0.85rem;
  color: var(--text-light);
  font-style: italic;
}

/* Social Section */
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

.social-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
  gap: 2rem;
  max-width: 800px;
  margin: 0 auto;
}

.social-card {
  background: var(--bg-primary);
  border-radius: var(--border-radius-xl);
  padding: 2rem;
  text-align: center;
  box-shadow: var(--shadow-lg);
  border: 1px solid var(--border-color);
  transition: all 0.4s cubic-bezier(0.4, 0, 0.2, 1);
  position: relative;
  overflow: hidden;
}

.social-card::before {
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

.social-card:hover::before {
  transform: scaleX(1);
}

.social-card:hover {
  transform: translateY(-8px);
  box-shadow: var(--shadow-2xl);
  border-color: var(--primary-color);
}

.social-icon-wrapper {
  width: 80px;
  height: 80px;
  margin: 0 auto 1.5rem;
  background: linear-gradient(135deg, rgba(99, 102, 241, 0.1) 0%, rgba(139, 92, 246, 0.1) 100%);
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  transition: all 0.3s ease;
}

.social-card:hover .social-icon-wrapper {
  background: var(--gradient-primary);
  transform: scale(1.1) rotate(5deg);
}

.social-icon {
  font-size: 2rem;
  filter: drop-shadow(0 2px 4px rgba(99, 102, 241, 0.2));
}

.qr-code-placeholder {
  background: var(--bg-secondary);
  border: 2px dashed var(--border-color);
  border-radius: var(--border-radius-md);
  padding: 1.5rem;
  margin: 1rem 0;
  min-height: 180px;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  transition: all 0.3s ease;
}

.social-card:hover .qr-code-placeholder {
  border-color: var(--primary-color);
  background: rgba(99, 102, 241, 0.05);
}

.qr-icon {
  font-size: 2.5rem;
  margin-bottom: 0.75rem;
  filter: drop-shadow(0 2px 4px rgba(99, 102, 241, 0.2));
}

.qr-code-placeholder p {
  font-size: 0.9rem;
  color: var(--text-light);
}

.social-card h3 {
  font-size: 1.3rem;
  font-weight: 700;
  color: var(--text-dark);
  margin-bottom: 0.5rem;
  letter-spacing: -0.01em;
  background: var(--gradient-primary);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
}

.social-card > p {
  color: var(--text-light);
  line-height: 1.7;
  font-size: 0.95rem;
}

/* Responsive */
@media (max-width: 968px) {
  .contact-layout {
    grid-template-columns: 1fr;
    gap: 2rem;
  }
  
  .map-placeholder {
    min-height: 300px;
  }
}

@media (max-width: 768px) {
  .contact-hero {
    padding: 40px 0;
  }
  
  .info-card {
    padding: 2rem 1.5rem;
  }
  
  .info-item {
    flex-direction: column;
    text-align: center;
    gap: 1rem;
  }
  
  .info-icon-wrapper {
    margin: 0 auto;
  }
  
  .map-card {
    padding: 2rem 1.5rem;
  }
  
  .social-grid {
    grid-template-columns: 1fr;
    gap: 1.5rem;
  }
  
  .social-card {
    padding: 1.5rem;
  }
}
</style>

