<template>
  <div class="home">
    <h1>ยินดีต้อนรับสู่กิจกรรมที่น่าสนใจของนักศึกษา</h1>
    <p>สำรวจกิจกรรมต่างๆ และค้นหาความสนใจของคุณ!</p>
    <router-link to="/info">เรียนรู้เพิ่มเติม</router-link>
    <router-link to="/register">ลงทะเบียนตอนนี้</router-link>
    <router-link to="/contact">ติดต่อเรา</router-link>
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue';

export default defineComponent({
  name: 'HomeComponent',
});
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Kanit:wght@700&family=Prompt:wght@400;600&family=Mali:wght@700&display=swap');

.home {
  text-align: center;
  margin-top: 50px;
  font-family: 'Mali', 'Prompt', 'Kanit', sans-serif;
  animation: fadeIn 1.2s;
  background: linear-gradient(120deg, #f6d365 0%, #fda085 100%);
  border-radius: 24px;
  box-shadow: 0 8px 32px rgba(253,160,133,0.15);
  padding: 40px 0 30px 0;
  max-width: 600px;
  margin-left: auto;
  margin-right: auto;
}

@keyframes fadeIn {
  from { opacity: 0; transform: translateY(-30px);}
  to { opacity: 1; transform: translateY(0);}
}

h1 {
  font-size: 2.7em;
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
  font-size: 1.3em;
  color: #ff9966;
  margin-bottom: 30px;
  font-family: 'Prompt', sans-serif;
}

/* ใช้ a แทน router-link */
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
</style>