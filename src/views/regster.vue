<script setup>
function Signal() {
  const name = document.getElementById('name').value.trim();
  const email = document.getElementById('email').value.trim();
  const password = document.getElementById('password').value.trim();
  const confirmPassword = document.getElementById('confirm').value.trim();
  const date = document.getElementById('date').value;
  const gender = document.getElementById('select').value;
  const result = document.getElementById('result');

  if (password.length >= 4  && gender && date) {
    result.innerHTML = "Sign up is correct";
    result.style.color = "green";
    router.push({ path: '/contact' }) 
  } else {
    result.innerHTML = "Sign up is incorrect";
    result.style.color = "red";
  }
}
</script>

<template>
  <fieldset class="container">
      Name
      <input type="text" placeholder="Enter your full name" id="name" /><br><br>
      Email
      <input type="email" placeholder="Enter your email" id="email" /><br><br>
      Date
      <input type="date" id="date" /><br><br>
      Gender
   <select id="select">
        <option value="">Select gender</option>
        <option value="male">Male</option>
        <option value="female">Female</option>
        <option value="others">Others</option>
      </select><br><br>
      Password
      <input type="password" placeholder="Create password" id="password" /><br><br>
    <button @click="Signal()">Sign Up</button>
  </fieldset>

  <p id="result"></p>
</template>

<style scoped>
.container {
  margin-top: 3%;
  text-align: center;
  margin-left: 30%;
  background-color: #06466388;
  width: 500px;
  border-radius: 7px;
  padding: 20px;
}

input,select {
  border-radius: 7px;
  border: none;
  color: #000;
  background-color: white;
  width: 470px;
  height: 27px;
}

#result {
  margin-top: 1%;
  text-align: center;
}

button {
  background-color: rgba(45, 45, 235, 0.979);
  border: none;
  border-radius: 7px;
  width: 477px;
  height: 30px;
  color: white;
  font-weight: bold;
  cursor: pointer;
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
