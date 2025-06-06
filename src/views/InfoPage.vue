<template>
  <div class="info-bg">
    <div class="info-page">
      <h1>📚 ข้อมูลเกี่ยวกับกิจกรรม</h1>
      <p>
        👋 ยินดีต้อนรับสู่หน้าข้อมูลกิจกรรมที่น่าสนใจสำหรับนักศึกษา <br>
        ที่นี่คุณจะพบรายละเอียดเกี่ยวกับกิจกรรมต่างๆ ที่จัดขึ้นสำหรับนักศึกษา
      </p>
      <ul>
        <li>⚽ กิจกรรม 1: กีฬาและสุขภาพ – สนุกกับการออกกำลังกายและสร้างทีมเวิร์ค!</li>
        <li>🎵 กิจกรรม 2: ดนตรีและศิลปะ – ปลดปล่อยความคิดสร้างสรรค์!</li>
        <li>🤝 กิจกรรม 3: อาสาสมัคร – สร้างสังคมที่ดีและช่วยเหลือผู้อื่น!</li>
      </ul>
      <div class="emoji-animate">✨🌟🎉</div>
    </div>
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue';

export default defineComponent({
  name: 'InfoPage',
});
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Kanit:wght@700&family=Prompt:wght@400;600&display=swap');

.info-bg {
  min-height: 90vh;
  width: 99vw;
  background: linear-gradient(135deg, #00FFFF 0%, #ff5858 100%);
  display: flex;
  align-items: center;
  justify-content: center;
  padding: 0;
  margin: 0;
}

.info-page {
  max-width: 600px;
  margin: 40px auto;
  padding: 36px 32px 28px 32px;
  background: linear-gradient(120deg, #f9d423 0%, #ff4e50 100%);
  border-radius: 22px;
  box-shadow: 0 8px 32px rgba(255,78,80,0.10);
  font-family: 'Prompt', 'Kanit', sans-serif;
  animation: fadeIn 1s;
}

@keyframes fadeIn {
  from { opacity: 0; transform: translateY(-30px);}
  to { opacity: 1; transform: translateY(0);}
}

h1 {
  text-align: center;
  font-family: 'Kanit', sans-serif;
  color: #ff4e50;
  margin-bottom: 50px;
  letter-spacing: 1px;
  text-shadow: 1px 2px 12px #fff3;
  font-size: 2em;
  animation: bounce 1.2s;
}

@keyframes bounce {
  0%   { transform: scale(0.9);}
  50%  { transform: scale(1.05);}
  100% { transform: scale(1);}
}

p {
  font-size: 1.15em;
  color: #fffbe7;
  margin-bottom: 24px;
  text-align: center;
  font-family: 'Prompt', sans-serif;
}

ul {
  list-style: none;
  padding: 0;
}

li {
  background: rgba(255,255,255,0.85);
  margin-bottom: 20px;
  padding: 20px 18px;
  border-radius: 25px;
  color: #ff4e50;
  font-family: 'Kanit', sans-serif;
  font-size: 1.08em;
  box-shadow: 0 2px 8px rgba(255,78,80,0.08);
  transition: transform 0.2s, box-shadow 0.2s;
  cursor: pointer;
  display: flex;
  align-items: center;
  gap: 10px;
}

li:hover {
  transform: scale(1.04) translateY(-2px);
  box-shadow: 0 4px 16px rgba(255,78,80,0.18);
  background: #fffbe7;
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