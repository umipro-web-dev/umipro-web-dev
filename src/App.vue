<template>
  <div id="app">
    <header>
      <div class="header-container">
        <div class="logo-section">
          <span class="logo-icon">⚡</span>
          <h1 class="site-title">DevFlow</h1>
        </div>
        <nav class="nav-section">
          <button class="btn btn-login">ログイン</button>
          <button class="btn btn-signup">新規登録</button>
        </nav>
      </div>
    </header>
    
    <main class="main-content">
      <div class="hero-section">
        <div class="hero-content">
          <h2 class="hero-title">開発を流れるように</h2>
          <p class="hero-subtitle">DevFlow で最高の開発体験を実現</p>
          
          <div class="cta-buttons">
            <button class="btn btn-signup btn-large">今すぐ新規登録</button>
            <button class="btn btn-login-large btn-large">ログインはこちら</button>
          </div>
        </div>
      </div>
    </main>
  </div>
</template>

<script setup>
</script>

<style>
html, body, div#__nuxt, div#app {
  width: 100%;
  height: 100%;
  padding: 0;
  margin: 0;
  background-color: #16171d;
  font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
}

header {
  width: 100%;
  background-color: #16171d;
  height: 10vh;
  border-bottom: 2px solid #525257;
  display: flex;
  align-items: center;
  padding: 0;
  box-sizing: border-box;
}

.header-container {
  width: 100%;
  max-width: 1400px;
  margin: 0 auto;
  padding: 0 2rem;
  display: flex;
  justify-content: space-between;
  align-items: center;
  box-sizing: border-box;
}

.logo-section {
  display: flex;
  align-items: center;
  gap: 0.75rem;
  cursor: pointer;
  transition: opacity 0.3s ease;
}

.logo-section:hover {
  opacity: 0.8;
}

.logo-icon {
  font-size: 1.75rem;
  animation: pulse 2s ease-in-out infinite;
}

@keyframes pulse {
  0%, 100% {
    opacity: 1;
  }
  50% {
    opacity: 0.7;
  }
}

.site-title {
  font-size: 1.5rem;
  font-weight: 700;
  margin: 0;
  background: linear-gradient(135deg, #64e1dc 0%, #7c3aed 100%);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
}

.nav-section {
  display: flex;
  gap: 1rem;
  align-items: center;
}

.btn {
  padding: 0.625rem 1.25rem;
  border: none;
  border-radius: 0.5rem;
  font-size: 0.95rem;
  font-weight: 600;
  cursor: pointer;
  transition: all 0.3s ease;
  outline: none;
}

.btn-login {
  background-color: transparent;
  color: #a1a1a6;
  border: 1.5px solid #525257;
}

.btn-login:hover {
  background-color: rgba(82, 82, 87, 0.1);
  border-color: #64e1dc;
  color: #64e1dc;
  transform: translateY(-2px);
}

.btn-signup {
  background: linear-gradient(135deg, #64e1dc 0%, #7c3aed 100%);
  color: #ffffff;
  border: none;
}

.btn-signup:hover {
  opacity: 0.9;
  box-shadow: 0 8px 24px rgba(100, 225, 220, 0.4);
  transform: translateY(-2px);
}

.btn:active {
  transform: translateY(0);
}

/* Main Content */
.main-content {
  width: 100%;
  height: calc(100% - 10vh);
  display: flex;
  align-items: center;
  justify-content: center;
  padding: 2rem;
  box-sizing: border-box;
}

.hero-section {
  width: 100%;
  max-width: 1000px;
  text-align: center;
  animation: fadeIn 0.8s ease-out;
}

@keyframes fadeIn {
  from {
    opacity: 0;
    transform: translateY(20px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

.hero-content {
  display: flex;
  flex-direction: column;
  gap: 2rem;
}

.hero-title {
  font-size: 3.5rem;
  font-weight: 800;
  margin: 0;
  background: linear-gradient(135deg, #64e1dc 0%, #7c3aed 100%);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
  line-height: 1.2;
}

.hero-subtitle {
  font-size: 1.25rem;
  color: #a1a1a6;
  margin: 0;
  line-height: 1.6;
}

.cta-buttons {
  display: flex;
  gap: 1.5rem;
  justify-content: center;
  flex-wrap: wrap;
}

.btn-large {
  padding: 1rem 2.5rem;
  font-size: 1.1rem;
  border-radius: 0.75rem;
}

.btn-login-large {
  background-color: transparent;
  color: #a1a1a6;
  border: 2px solid #525257;
}

.btn-login-large:hover {
  background-color: rgba(82, 82, 87, 0.1);
  border-color: #64e1dc;
  color: #64e1dc;
  transform: translateY(-3px);
  box-shadow: 0 8px 24px rgba(100, 225, 220, 0.2);
}

@media (max-width: 768px) {
  .header-container {
    padding: 0 1rem;
  }

  .site-title {
    font-size: 1.25rem;
  }

  .btn {
    padding: 0.5rem 1rem;
    font-size: 0.85rem;
  }

  .logo-icon {
    font-size: 1.5rem;
  }

  .hero-title {
    font-size: 2rem;
  }

  .hero-subtitle {
    font-size: 1rem;
  }

  .cta-buttons {
    gap: 1rem;
  }

  .btn-large {
    padding: 0.875rem 1.75rem;
    font-size: 1rem;
    width: 100%;
  }
}
</style>