<script setup>
</script>

<template>
  <div class="home-container">
    <h1>Welcome to ElectroHUB⚡</h1>
    <p>If you buy products here, you get extra rewards and unbeatable deals!</p>
    <button @click="$router.push('/product')">Shop Now</button>
  </div>
  <div class="yyy">
    <h3>ElectroHUB⚡</h3>
        <p class="pp">Get the best electronics with unbeatable deals and reliable support.</p> <p class="pp">
           We’re here to power your tech journey.</p>
  </div>
</template>

<style scoped>
.home-container {
  background-color: aqua;
  padding: 3rem;
  border-radius: 12px;
  text-align: center;
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
  margin: 2rem;
}

h1 {
  color: #064663;
  margin-bottom: 1rem;
  font-size: 2rem;
}

p {
  color: #033649;
  font-size: 1.2rem;
  margin-bottom: 2rem;
}

button {
  background-color: #0077b6;
  color: white;
  border: none;
  padding: 0.8rem 1.5rem;
  font-size: 1rem;
  border-radius: 8px;
  cursor: pointer;
  transition: background-color 0.3s ease;
}

button:hover {
  background-color: #023e8a;
}
.yyy{
  background-color: #033649;
  color: #e3edf1;
  text-align: center;
}
.pp{
  color: #f1f1f1;
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
