<template>
  <footer class="footer">
    <div class="container">
      <div class="footer-content">
        <div class="footer-section">
          <h3>合末</h3>
          <p class="slogan">合抱之木，始于毫末</p>
          <p class="description">专业金融服务，助力企业发展</p>
        </div>
        <div class="footer-section">
          <h4>快速链接</h4>
          <ul>
            <li><router-link to="/">首页</router-link></li>
            <li><router-link to="/about">公司简介</router-link></li>
            <li><router-link to="/services">产品服务</router-link></li>
            <li><router-link to="/contact">联系我们</router-link></li>
          </ul>
        </div>
        <div class="footer-section">
          <h4>联系方式</h4>
          <p>电话：400-XXX-XXXX</p>
          <p>邮箱：info@hemo.com</p>
        </div>
      </div>
      <div class="footer-bottom">
        <p>&copy; 2024 合末. 保留所有权利.</p>
      </div>
    </div>
  </footer>
</template>

<script setup>
</script>

<style scoped>
.footer {
  background: linear-gradient(180deg, var(--bg-dark) 0%, #1a1f2e 100%);
  color: white;
  padding: 4rem 0 1.5rem;
  margin-top: auto;
  position: relative;
  overflow: hidden;
}

.footer::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  height: 1px;
  background: var(--gradient-primary);
  opacity: 0.3;
}

.footer-content {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: 2rem;
  margin-bottom: 2rem;
}

.footer-section h3 {
  font-size: 1.75rem;
  margin-bottom: 1.25rem;
  background: var(--gradient-primary);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
  font-weight: 800;
  letter-spacing: -0.02em;
}

.footer-section h4 {
  font-size: 1.1rem;
  margin-bottom: 1rem;
}

.slogan {
  font-size: 1.15rem;
  font-style: italic;
  background: var(--gradient-primary);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
  margin-bottom: 0.75rem;
  font-weight: 500;
}

.description {
  color: #9ca3af;
}

.footer-section ul {
  list-style: none;
}

.footer-section ul li {
  margin-bottom: 0.5rem;
}

.footer-section a {
  color: #9ca3af;
  text-decoration: none;
  transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
  position: relative;
  display: inline-block;
  padding-left: 0;
}

.footer-section a::before {
  content: '→';
  position: absolute;
  left: -20px;
  opacity: 0;
  transition: all 0.3s ease;
  color: var(--primary-color);
}

.footer-section a:hover {
  color: var(--primary-light);
  padding-left: 20px;
  transform: translateX(5px);
}

.footer-section a:hover::before {
  opacity: 1;
  left: 0;
}

.footer-section p {
  color: #9ca3af;
  margin-bottom: 0.5rem;
}

.footer-bottom {
  text-align: center;
  padding-top: 2.5rem;
  border-top: 1px solid rgba(255, 255, 255, 0.1);
  color: #9ca3af;
  font-size: 0.9rem;
  position: relative;
}

.footer-bottom::before {
  content: '';
  position: absolute;
  top: 0;
  left: 50%;
  transform: translateX(-50%);
  width: 100px;
  height: 1px;
  background: var(--gradient-primary);
  opacity: 0.5;
}

@media (max-width: 768px) {
  .footer-content {
    grid-template-columns: 1fr;
  }
}
</style>

