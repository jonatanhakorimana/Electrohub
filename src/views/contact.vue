<script setup>
   function send(){
    alert('Thank for to writting');
   }
</script>
<template>
   <fieldset class="container">
      <h2>contact us</h2>
      <h3>Do you want everything from this company?</h3>
      <div class="ggg">
        <div class="fff"><strong>📍Address</strong><br>
           location:Kigali/Nyabugogo <br>
          branche:Gisenyi/byahi
        </div>
        <div class="fff"><strong>📞Phone</strong> <br>:+250 795 503 938 / <br> :+250 789 595 673</div>
        <div class="fff"><strong>📨Email </strong><br> :elctroHUB@gmail.com /<br>
            This website
        </div>
      </div><br><br>
      Name: <input type="text" placeholder="nathan drip" required><br><br>
      Email: <input type="email" placeholder="email" required><br><br>
      Write <textarea name="" id="" placeholder="enter your message ..." required></textarea> <br><br>   
      <button  @click="send()">Send</button>
   </fieldset>
</template>

<style scoped>

 .container{
    margin-left: 30%;
    margin-top: 3%;
    border-radius: 7px;
    border: 0ch;
    background-color: rgba(128, 128, 128, 0.534);
    backdrop-filter: blur(20px);
    width: 500px;
    text-align: center;
    padding: 20px;
 }
 .ggg{
    display: flex;
    border-radius: 7px;
    justify-content: space-between;
 }
 button{
    width: 495px;
    border-radius: 7px;
    height: 27px;
    background-color: rgb(38, 38, 207);
    color: white;
    border: 0ch;
 }
 input {
    width: 490px;
    color: rgb(5, 4, 4);
    background-color: white;
    border: 0ch;
    height: 25px;
    border-radius: 7px;
 } 
 textarea{
    width: 495px;
    border-radius: 7px;
    color: rgb(5, 4, 4);
    border: 0ch;
    background-color: white; 
    height: 30px;
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