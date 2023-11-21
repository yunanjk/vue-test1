<template>
  <div class="about">
    <h1>This is an about page</h1>
    <KossieCoder>
      <!-- 'v-slot:'을 '#'으로 대체 가능 -->
      <!-- 자식컴포넌트에서 데이터를 받아오고 싶으면 #header="props" props 지정해주면됨  -->
      <template #header="props">
        <!-- slot 이름이 header인 부분에 출력될 코드 -->
        <p>header slot {{ props.kossie }}</p>
      </template>
      <template v-slot:default>
        <!-- slot 이름이 없는 default 부분에 출력될 코드 -->
        <p>slot</p>
      </template>
    </KossieCoder>
  </div>
</template>

<script>
import KossieCoder from "@/components/KossieCoder.vue";

export default {
  components: {
    KossieCoder
  }
}
</script>

<style>

</style>
