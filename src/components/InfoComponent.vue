<template>
  <div class="info-container">
    <h1>กิจกรรมนักศึกษาที่สนใจ</h1>
    <p>ยินดีต้อนรับสู่แพลตฟอร์มกิจกรรมที่น่าสนใจสำหรับนักศึกษา ที่นี่คุณจะพบกิจกรรมต่างๆ มากมายให้เลือกทำ</p>
    <h2>กิจกรรมที่มีจำหน่าย</h2>
    <ul>
      <li>กีฬา</li>
      <li>ศิลปะและหัตถกรรม</li>
      <li>เพลง</li>
      <li>ชมรมวิทยาศาสตร์</li>
      <li>บริการชุมชน</li>
    </ul>
    <p>เข้าร่วมกับเราเพื่อสำรวจความสนใจของคุณและพบเพื่อนใหม่!</p>
  </div>
</template>

<script lang="ts">
export default {
  name: 'InfoComponent',
};
</script>

<style scoped>
.info-container {
  padding: 20px;
  background-color: #f9f9f9;
  border-radius: 8px;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
}

h1 {
  color: #333;
}

h2 {
  color: #555;
}

ul {
  list-style-type: none;
  padding: 0;
}

li {
  margin: 5px 0;
}
</style>