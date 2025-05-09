<script setup>
import { ref } from 'vue';
import { useRouter } from 'vue-router';

const router = useRouter();

// Cart state to hold the added products
const cart = ref([]);

// List of products
const products = [
  {
    name: 'Laptop X1',
    image: 'https://i.pinimg.com/736x/eb/b3/5d/ebb35d9572ffff815578498fcf59cbbb.jpg',
  },
  {
    name: 'Headphones Pro',
    image: 'https://i.pinimg.com/736x/d7/cd/ec/d7cdec94bb1a046f03e1ac36fbd7b7f6.jpg',
  },
  {
    name: 'Smartwatch 3',
    image: 'https://i.pinimg.com/736x/08/3e/73/083e73ffbe321b6d18db54a46fdd61fb.jpg',
  },
  {
    name: 'Gaming Mouse',
    image: 'https://i.pinimg.com/736x/f9/20/06/f920067f7d78218df227e9faaf7529ea.jpg',
  },
  {
    name: 'Keyboard K2',
    image: 'https://i.pinimg.com/736x/e2/2a/3e/e22a3ea7f6822052ddac9ea14f1d6031.jpg',
  },
  {
    name: 'Monitor Ultra',
    image: 'https://i.pinimg.com/736x/c1/58/e1/c158e17fa982c0b9ccb2485ef173479a.jpg',
  },
  {
    name: 'I phone 15 plus',
    image: 'https://i.pinimg.com/736x/20/1b/97/201b97f47ba47078690c9ae9820fdeb3.jpg',
  },
];

// Function to add a product to the cart
const addToCart = (product) => {
  cart.value.push(product);
  alert(`${product.name} added to cart!`);
};

const goToLaptop = () => {
  router.push('/laptop');
};
</script>

<template>
  <div class="home-container">
    <h3>This is the product we have</h3>
  </div>

  <section class="sect">
    <div class="photo" v-for="(product, index) in products" :key="index">
      <img :src="product.image" :alt="product.name" />
      <p>{{ product.name }}</p>
      <button class="blue" @click="addToCart(product)">Add to cart</button>
    </div>
  </section>

  <!-- Cart Section -->
  <section v-if="cart.length" class="cart-section">
    <h4>Items in Cart: {{ cart.length }}</h4>
    <ul>
      <li v-for="(item, index) in cart" :key="index">
        {{ item.name }}
      </li>
    </ul>
  </section>

  <footer class="footer">
    <div class="footer-content">
      <div class="footer-section about">
        <h3>ElectroHUB⚡</h3>
        <p>Get the best electronics with unbeatable deals and reliable support. We’re here to power your tech journey.</p>
      </div>

      <div class="footer-section links">
        <h4>Quick Links</h4>
        <ul>
          <li><a href="/">Home</a></li>
          <li><a href="/laptop">Shop</a></li>
          <li><a href="/contact">Contact</a></li>
          <li><a href="/about">About Us</a></li>
        </ul>
      </div>

      <div class="footer-section contact">
        <h4>Contact</h4>
        <p>📞 +250 795 503 938</p>
        <p>📧 electrohub@gmail.com</p>
        <p>📍 Kigali, Rwanda</p>
      </div>
    </div>
    <div class="footer-bottom">
      <p>&copy; 2025 ElectroHUB. All rights reserved.</p>
    </div>
  </footer>
</template>

<style scoped>
.home-container {
  background-color: rgb(13, 224, 126);
  text-align: center;
  height: 70px;
  display: flex;
  justify-content: center;
  align-items: center;
}

h3 {
  font-weight: 100;
  font-size: 20px;
}

.sect {
  display: flex;
  flex-wrap: wrap;
  gap: 20px;
  justify-content: center;
  padding: 2rem;
}

.photo {
  width: 250px;
  border: 1px solid #ccc;
  border-radius: 8px;
  padding: 1rem;
  text-align: center;
  background-color: #f9f9f9;
  height: 340px;
}

.photo img {
  max-width: 100%;
  height: auto;
  margin-bottom: 1rem;
}

.blue {
  background-color: rgb(36, 100, 237);
  color: white;
  border: none;
  padding: 0.5rem 1rem;
  border-radius: 7px;
  cursor: pointer;
}

.blue:hover {
  background-color: #1d4ed8;
}

.cart-section {
  padding: 1rem;
  background-color: #f4f4f4;
  border: 1px solid #ccc;
  margin-top: 2rem;
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
