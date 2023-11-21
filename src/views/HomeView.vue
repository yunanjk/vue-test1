<template>
  <div>
    <h1>This is home page</h1>
    <!-- <p>{{ name }}</p> -->
    <KossieCoder title="home title" age="25"/>
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


<style scoped lang="scss">
// style scoped lang="scss" : 현재 파일에서만 style 적용시킨다는 뜻
h1 {
  color: red;
}
</style>
