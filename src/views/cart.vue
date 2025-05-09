<template>
    <div class="cart-container">
      <h2>Your Cart</h2>
      <div v-if="cart.length === 0">
        <p>Your cart is empty.</p>
        <router-link to="/">Go back to Shop</router-link>
      </div>
      <div v-else>
        <ul>
          <li v-for="(item, index) in cart" :key="index">
            <div class="cart-item">
              <img :src="item.image" :alt="item.name" />
              <p>{{ item.name }}</p>
              <button @click="removeFromCart(index)">Remove</button>
            </div>
          </li>
        </ul>
        <div class="cart-summary">
          <p>Total Items: {{ cart.length }}</p>
          <button class="checkout-button">Proceed to Checkout</button>
        </div>
      </div>
    </div>
  </template>
  
  <script setup>
  import { ref, onMounted } from 'vue';
  
  const cart = ref([]);
  
  // Load the cart from localStorage when the page is loaded
  onMounted(() => {
    const savedCart = JSON.parse(localStorage.getItem('cart')) || [];
    cart.value = savedCart;
  });
  
  // Remove item from cart and update localStorage
  const removeFromCart = (index) => {
    cart.value.splice(index, 1);
    localStorage.setItem('cart', JSON.stringify(cart.value)); // Save updated cart to localStorage
  };
  </script>
  
  <style scoped>
  .cart-container {
    padding: 2rem;
    max-width: 900px;
    margin: auto;
    text-align: center;
  }
  
  .cart-item {
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin: 1rem 0;
  }
  
  .cart-item img {
    width: 50px;
    height: auto;
    margin-right: 1rem;
  }
  
  .checkout-button {
    background-color: rgb(36, 100, 237);
    color: white;
    padding: 0.5rem 1rem;
    border: none;
    border-radius: 5px;
    cursor: pointer;
    margin-top: 1rem;
  }
  
  .checkout-button:hover {
    background-color: #1d4ed8;
  }
  </style>
  