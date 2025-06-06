<template>
  <div class="register">
    <h1>ลงทะเบียนเข้าร่วมกิจกรรม</h1>
    <form @submit.prevent="submitRegistration">
      <div>
        <label for="name">ชื่อ:</label>
        <input type="text" id="name" v-model="name" required />
      </div>
      <div>
        <label for="email">อีเมล:</label>
        <input type="email" id="email" v-model="email" required />
      </div>
      <div>
        <label for="activity">เลือกกิจกรรม:</label>
        <select id="activity" v-model="selectedActivity" required>
          <option v-for="activity in activities" :key="activity" :value="activity">{{ activity }}</option>
        </select>
      </div>
      <button type="submit">ลงทะเบียน</button>
    </form>
    <p v-if="message">{{ message }}</p>
  </div>
</template>

<script lang="ts">
import { defineComponent, ref } from 'vue';

export default defineComponent({
  name: 'RegisterComponent',
  setup() {
    const name = ref('');
    const email = ref('');
    const selectedActivity = ref('');
    const activities = ref(['Sports', 'Music', 'Art', 'Science']);
    const message = ref('');

    const submitRegistration = () => {
      message.value = `Thank you, ${name.value}! You have registered for ${selectedActivity.value}.`;
      name.value = '';
      email.value = '';
      selectedActivity.value = '';
    };

    return {
      name,
      email,
      selectedActivity,
      activities,
      message,
      submitRegistration,
    };
  },
});
</script>

<style scoped>
.register {
  max-width: 400px;
  margin: auto;
  padding: 20px;
  border: 1px solid #ccc;
  border-radius: 5px;
  background-color: #f9f9f9;
}

h1 {
  text-align: center;
}

form div {
  margin-bottom: 15px;
}

label {
  display: block;
  margin-bottom: 5px;
}

input, select {
  width: 100%;
  padding: 8px;
  box-sizing: border-box;
}

button {
  width: 100%;
  padding: 10px;
  background-color: #28a745;
  color: white;
  border: none;
  border-radius: 5px;
  cursor: pointer;
}

button:hover {
  background-color: #218838;
}
</style>