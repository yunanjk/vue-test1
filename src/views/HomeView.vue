<template>
  <div>
    <h1>This is home page</h1>
    <!-- <p>{{ name }}</p> -->
    <KossieCoder />
  </div>
</template>

<script>
// @/ : src 폴더 뜻함
import KossieCoder from '@/components/KossieCoder.vue';

export default {
  name: 'HomeView',
  data() {
    return {
      name: "Kossie Coder"
    }
  },
  components: {
    KossieCoder
  }
}
</script>

<style>
h1 {
  color: red;
}
</style>
