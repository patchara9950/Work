<template>
  <div class="home-bg">
    <div class="home-page">
      <h1>🎉 ยินดีต้อนรับสู่กิจกรรมที่🎓</h1>
      <p> สำรวจกิจกรรมต่างๆ และค้นหาความหลงใหลของคุณ! </p>
      <router-link to="/info">🔎 Learn More</router-link>
      <router-link to="/contact">📬 Contact Us</router-link>
      <router-link to="/register">📝 Register Now</router-link>
      <div class="emoji-animate">🥳🌟🎈</div>
    </div>
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue';

export default defineComponent({
  name: 'HomePage',
});
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Kanit:wght@700&family=Prompt:wght@400;600&family=Mali:wght@700&display=swap');

.home-bg {
  min-height: 100vh;
  width: 100vw;
  background: linear-gradient(135deg, #00FFFF 0%, #ff5858 100%);
  display: flex;
  align-items: center;
  justify-content: center;
  padding: 0;
  margin: 0;
  overflow: hidden;
}

.home-page {
  text-align: center;
  font-family: 'Mali', 'Prompt', 'Kanit', sans-serif;
  animation: fadeIn 1.2s;
  background: linear-gradient(120deg, #f6d365 0%, #fda085 100%);
  border-radius: 50px;
  box-shadow: 0 8px 32px rgba(253,160,133,0.15);
  padding: 40px 0 30px 0;
  max-width: 600px;
  width: 100%;
  margin-left: auto;
  margin-right: auto;
  position: relative;
}

@keyframes fadeIn {
  from { opacity: 0; transform: translateY(-30px);}
  to { opacity: 1; transform: translateY(0);}
}

h1 {
  font-size: 2.3em;
  color: #ff5e62;
  font-family: 'Mali', cursive;
  letter-spacing: 2px;
  text-shadow: 2px 2px 12px #fff3;
  margin-bottom: 20px;
  animation: bounce 1.2s;
}

@keyframes bounce {
  0%   { transform: scale(0.9);}
  50%  { transform: scale(1.05);}
  100% { transform: scale(1);}
}

p {
  font-size: 1.25em;
  color:rgb(0, 0, 0);
  margin-bottom: 30px;
  font-family: 'Prompt', sans-serif;
  animation: fadeIn 2s;
}

a {
  display: inline-block;
  margin: 10px;
  text-decoration: none;
  color: #fff !important;
  font-weight: 700;
  font-size: 1.15em;
  padding: 10px 22px;
  border-radius: 24px;
  background: linear-gradient(90deg, #f857a6 0%, #ff5858 100%);
  transition: background 0.3s, color 0.3s, transform 0.2s, box-shadow 0.2s;
  box-shadow: 0 2px 8px rgba(255,88,88,0.12);
  font-family: 'Kanit', sans-serif;
  letter-spacing: 1px;
}

a:hover {
  background: linear-gradient(90deg, #ff5858 0%, #f857a6 100%);
  color: #fffbe7 !important;
  transform: translateY(-3px) scale(1.08) rotate(-2deg);
  box-shadow: 0 4px 16px rgba(255,88,88,0.22);
}

.emoji-animate {
  text-align: center;
  font-size: 2.2em;
  margin-top: 18px;
  animation: emojiPop 1.2s infinite alternate;
}

@keyframes emojiPop {
  0% { transform: scale(1);}
  60% { transform: scale(1.18) rotate(-8deg);}
  100% { transform: scale(1);}
}
</style>