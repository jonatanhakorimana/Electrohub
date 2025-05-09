<template>
  <section class="about-section">
    <h1>About ⚡ElectroHub</h1>
    <p>Welcome to <span class="highlight">Electro Hub</span> — your one-stop destination for the latest and greatest in electronics.</p>
    <p>We specialize in top-quality gadgets, smart devices, and tech accessories that make life <strong>easier</strong>, <strong>faster</strong>, and more connected.</p>
    <p>At <span class="highlight">Electro Hub</span>, we believe technology should be <em>accessible</em>, <em>reliable</em>, and <em>inspiring</em>. That’s why we carefully curate a wide range of products — all at competitive prices.</p>
    <p>Driven by <strong>innovation</strong> and <strong>customer satisfaction</strong>, our mission is to bring cutting-edge tech to your doorstep with fast delivery and excellent service.</p>
    <button class="cta-button" @click="learnMore">Learn More</button>
  </section>
</template>

<script>
export default {
  name: 'AboutElectroHub',
  methods: {
    learnMore() {
      alert('Thank you for your interest! Visit our product page to explore more.');
    }
  }
}
</script>

<style scoped>
.about-section {
  max-width: 900px;
  margin: 60px auto;
  padding: 40px;
  background: #fff;
  border-radius: 12px;
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
}

.about-section h1 {
  font-size: 2.5rem;
  background-color: #1976d2;
  color: #0d0f12;
  margin-bottom: 20px;
  text-align: center;
}

.about-section p {
  font-size: 1.1rem;
  line-height: 1.7;
  margin-bottom: 20px;
}

.highlight {
  color: #1976d2;
  font-weight: bold;
}

.cta-button {
  display: block;
  width: max-content;
  margin: 30px auto 0;
  padding: 12px 28px;
  font-size: 1rem;
  background-color: #1976d2;
  color: white;
  border: none;
  border-radius: 8px;
  cursor: pointer;
  transition: background 0.3s ease;
}

.cta-button:hover {
  background-color: #0d47a1;
}
.footer {
  background-color: #064663;
  color: #f1f1f1;
  padding: 2rem 1rem;
  font-family: 'Arial', sans-serif;
}

.footer-content {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
  gap: 2rem;
  max-width: 1100px;
  margin: auto;
}

.footer-section {
  flex: 1;
  min-width: 200px;
}

.footer-section h3,
.footer-section h4 {
  margin-bottom: 1rem;
  color: #00b4d8;
}

.footer-section ul {
  list-style: none;
  padding: 0;
}

.footer-section ul li {
  margin: 0.5rem 0;
}

.footer-section ul li a {
  color: #f1f1f1;
  text-decoration: none;
}

.footer-section ul li a:hover {
  text-decoration: underline;
}

.footer-bottom {
  text-align: center;
  margin-top: 2rem;
  font-size: 0.9rem;
  border-top: 1px solid rgba(255, 255, 255, 0.2);
  padding-top: 1rem;
}
</style>
