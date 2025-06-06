<template>
  <div class="contact-page">
    <ContactComponent />
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue';
import ContactComponent from '../components/ContactComponent.vue';

export default defineComponent({
  name: 'ContactPage',
  components: {
    ContactComponent
  }
});
</script>

<style scoped>
.contact-page {
  padding: 20px;
  text-align: center;
}
</style>