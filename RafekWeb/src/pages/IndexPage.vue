<template>
  <q-page class="landing-page">
    <header class="hero-section">
      <nav>
        <div class="logo center">
          <q-avatar size="150px" class="center">
            <img src="https://ucarecdn.com/c170e3b7-b034-44b3-a298-5fdea0ec8fb4/-/preview/500x500/" alt="Rafek Logo">
          </q-avatar>
        </div>
      </nav>
      <div class="hero-content">
        <div class="text-h1 center">RAFEK</div>
        <h1 class="text-h2">AI Guidance for a Sustainable Future</h1>
        <p class="text-h5 q-mt-md">Track, analyze, and reduce your company's carbon footprint with cutting-edge AI</p>
        <q-btn color="primary" label="Get Started" class="q-mt-xl" size="lg" />
      </div>
    </header>
    <section class="features">
      <div class="feature">
        <q-icon name="eco" size="4rem" color="green" />
        <h3>Carbon Tracking</h3>
        <p>Monitor your organization's carbon emissions across all sectors</p>
      </div>
      <div class="feature">
        <q-icon name="insert_chart" size="4rem" color="green" />
        <h3>Beautiful Dashboard</h3>
        <p>Visualize your carbon footprint data with intuitive charts and graphs</p>
      </div>
      <div class="feature">
        <q-icon name="psychology" size="4rem" color="green" />
        <h3>AI Predictions</h3>
        <p>Forecast future emissions and receive AI-powered recommendations</p>
      </div>
      <div class="feature">
        <q-icon name="smart_toy" size="4rem" color="green" />
        <h3>AI Strategies</h3>
        <p>Receive tailored strategies to reduce emissions and improve sustainability</p>
      </div>
    </section>
    <section class="cta-section">
      <q-btn color="secondary" label="Sign In" class="q-mr-md" size="lg" />
      <q-btn color="primary" label="Login" size="lg" />
    </section>
  </q-page>
</template>

<script setup>
import { defineOptions } from 'vue';

defineOptions({
  name: 'IndexPage'
});
</script>

<style lang="scss" scoped>
.landing-page {
  font-family: 'Poppins', sans-serif; 
  color: #2c3e50;
  background-color: #f0f8f0;
}

.hero-section {
  background: linear-gradient(135deg, #a7dda8, #81b5df);
  padding: 2rem;
  min-height: 80vh;
  display: flex;
  flex-direction: column;

  nav {
    display: flex;
    justify-content: center;    
    .logo {
      font-size: 2rem;
      font-weight: bold;
      color: white;
    }
  }

  .hero-content {
    flex-grow: 1;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    text-align: center;
    color: rgb(1, 71, 1);

    h1 {
      font-weight: 300;
      margin-bottom: 1rem;
      animation: fadeInUp 1s ease-out;
    }

    p {
      max-width: 600px;
      margin-bottom: 2rem;
      animation: fadeInUp 1s ease-out 0.5s both;
    }
    .text-h1 {
      font-size: 4rem;
      font-weight: 700;
      letter-spacing: 2px;
      text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.1);
      margin-bottom: 1rem;
    }
  }
}
.cta-section {
  background-color: white;
  padding: 4rem 2rem;
  display: flex;
  justify-content: center;
  align-items: center;
}

.features {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-around;
  padding: 4rem 2rem;
  background-color: white;

  .feature {
    text-align: center;
    max-width: 300px;
    width: calc(50% - 2rem);
    margin: 1rem;
    animation: fadeInUp 1s ease-out 1s both;
    transition: transform 0.3s ease, box-shadow 0.3s ease;
    padding: 1rem;
    border-radius: 8px;

    &:hover {
      box-shadow: 0 10px 20px rgba(0, 0, 0, 0.1);
      background: linear-gradient(135deg, #c9f1cb, #a0ccf1);
    }
  }
}

@media (max-width: 768px) {
  .features .feature {
    width: 100%;
  }
}


@keyframes fadeInUp {
  from {
    opacity: 0;
    transform: translateY(20px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}
</style>
