<script setup>

import { RouterLink, RouterView, useRouter } from 'vue-router'

const router = useRouter()
const toggleCart = () => {
  const sidebar = document.getElementById('cartSidebar')
  if (sidebar) {
    sidebar.style.right = sidebar.style.right === '0px' ? '-400px' : '0px'
  }
}

// Navigate based on product category selection
const handleProductChange = (event) => {
  const selected = event.target.value
  if (selected && selected !== '#') {
    router.push(selected)
  }
}
</script>
<template>
  <header class="navbar">
    <h2>ElectroHUB⚡</h2>
    <nav class="nav-links">
      <RouterLink to="/">Home</RouterLink>
      <RouterLink to="/product">product</RouterLink>
      <RouterLink to="/about">About</RouterLink>
      <RouterLink to="/contact">Contact</RouterLink>
      <RouterLink to="/regster">join now</RouterLink>
      <a href="#" @click.prevent="toggleCart">Cart 🛒</a>
    </nav>
  </header>

  <RouterView />
</template>

<style scoped>
header {
  margin-left: -20px;
  margin-top: -0.7%;
  background-color: rgb(0, 4, 255);
  padding: 1rem;
  color: rgb(242, 242, 250);
  display: flex;
  width: 100%;
  justify-content: space-between;
  align-items: center;
}

h2 {
  color: rgb(7, 127, 175);
  margin: 0;
}
a{
  color: rgb(55, 244, 55);
  text-decoration: none;
}
a:hover{
  transform: scale(1.2);
  text-decoration: underline;
}
.nav-links {
  display: flex;
  gap: 1rem;
  align-items: center;
}

select {
  padding: 0.4rem;
  border-radius: 5px;
  border: 1px solid #ccc;
}
</style>
