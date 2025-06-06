<template>
  <div class="register-bg">
    <div class="register-page">
      <h1>📝 ลงทะเบียนเข้าร่วมกิจกรรม</h1>
      <form @submit.prevent="handleSubmit">
        <div class="input-group">
          <label for="name">👤 ชื่อ:</label>
          <input type="text" id="name" v-model="formData.name" required />
        </div>
        <div class="input-group">
          <label for="email">📧 อีเมล:</label>
          <input type="email" id="email" v-model="formData.email" required />
        </div>
        <div class="input-group">
          <label for="activity">🎯 เลือกกิจกรรม:</label>
          <select id="activity" v-model="formData.activity" required>
            <option value="" disabled>เลือกกิจกรรม</option>
            <option value="sports">⚽ กีฬา</option>
            <option value="music">🎵 เพลง</option>
            <option value="art">🎨 ศิลปะ</option>
          </select>
        </div>
        <button type="submit">✅ สมัคร</button>
      </form>
      <transition name="fade">
        <div v-if="successMessage" class="success-message">{{ successMessage }}</div>
      </transition>
      <div class="emoji-animate">🎉✨🏆</div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      formData: {
        name: '',
        email: '',
        activity: ''
      },
      successMessage: ''
    };
  },
  methods: {
    handleSubmit() {
      this.successMessage = 'สมัครสำเร็จ! ขอบคุณที่ลงทะเบียนเข้าร่วมกิจกรรม 🎉';
      setTimeout(() => {
        this.successMessage = '';
      }, 3000);
      this.formData.name = '';
      this.formData.email = '';
      this.formData.activity = '';
    }
  }
};
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Kanit:wght@700&family=Prompt:wght@400;600&display=swap');

.register-bg {
  min-height: 100vh;
  width: 100vw;
  background: linear-gradient(135deg, #00FFFF 10%, #ff5858 100%);
  display: flex;
  align-items: center;
  justify-content: center;
  padding: 0;
  margin: 0;
  overflow: hidden;
}

.register-page {
  max-width: 540px;
  width: 100%;
  margin: 40px 16px;
  padding: 48px 40px 36px 40px;
  border-radius: 24px;
  background: linear-gradient(120deg, #f6d365 0%, #fda085 100%);
  box-shadow: 0 8px 32px rgba(253,160,133,0.18);
  font-family: 'Prompt', 'Kanit', sans-serif;
  animation: fadeIn 1s;
  position: relative;
}

@keyframes fadeIn {
  from { opacity: 0; transform: translateY(-30px);}
  to { opacity: 1; transform: translateY(0);}
}

.register-page h1 {
  text-align: center;
  font-family: 'Kanit', sans-serif;
  color: #ff5e62;
  margin-bottom: 24px;
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

.input-group {
  margin-bottom: 18px;
  display: flex;
  flex-direction: column;
  align-items: flex-start;
}

label {
  margin-bottom: 6px;
  font-weight: 600;
  color: #ff5858;
  font-family: 'Kanit', sans-serif;
  font-size: 1.08em;
  display: flex;
  align-items: center;
  gap: 4px;
}

input,
select {
  width: 100%;
  padding: 11px 1qqpx;
  border: none;
  border-radius: 8px;
  font-size: 1em;
  font-family: 'Prompt', sans-serif;
  background: #fffbe7;
  box-shadow: 0 2px 8px rgba(255,88,88,0.06);
  transition: box-shadow 0.2s, border 0.2s;
  outline: none;
}

input:focus,
select:focus {
  box-shadow: 0 0 0 2px #ffb88c;
  border: 1.5px solid #ff9966;
}

button {
  width: 100%;
  padding: 12px 0;
  background: linear-gradient(90deg, #f857a6 0%, #ff5858 100%);
  color: #fff;
  font-family: 'Kanit', sans-serif;
  font-size: 1.15em;
  font-weight: 700;
  border: none;
  border-radius: 24px;
  cursor: pointer;
  margin-top: 10px;
  box-shadow: 0 2px 8px rgba(255,88,88,0.12);
  transition: background 0.3s, transform 0.2s, box-shadow 0.2s;
  letter-spacing: 1px;
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 6px;
}

button:hover {
  background: linear-gradient(90deg, #ff5858 0%, #f857a6 100%);
  transform: translateY(-2px) scale(1.04);
  box-shadow: 0 4px 16px rgba(255,88,88,0.22);
}

.success-message {
  margin-top: 18px;
  padding: 12px 0;
  background: #fffbe7;
  color: #ff5858;
  border-radius: 16px;
  font-family: 'Kanit', sans-serif;
  font-size: 1.1em;
  text-align: center;
  animation: pop 0.5s;
  box-shadow: 0 2px 8px rgba(255,88,88,0.10);
}

@keyframes pop {
  0% { transform: scale(0.8); opacity: 0;}
  80% { transform: scale(1.08);}
  100% { transform: scale(1); opacity: 1;}
}

.emoji-animate {
  text-align: center;
  font-size: 2em;
  margin-top: 22px;
  animation: emojiPop 1.2s infinite alternate;
}

@keyframes emojiPop {
  0% { transform: scale(1);}
  60% { transform: scale(1.18) rotate(-8deg);}
  100% { transform: scale(1);}
}

.fade-enter-active, .fade-leave-active {
  transition: opacity 0.5s;
}
.fade-enter-from, .fade-leave-to {
  opacity: 0;
}
</style>