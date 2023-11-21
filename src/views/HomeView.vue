<template>
  <div>
    <h1>This is home page</h1>
    <InputField :name="name"/>
    <button @click="updateName">submit</button>
    {{ name }}
  </div>
</template>

<script>
import InputField from "@/components/InputField.vue";

export default {
  name: 'HomeView',
  components: {
    InputField
  },
  data() {
    return {
      name: "Kossie Coder"
    }
  },

  // 인스턴스 라이프사이클
  beforeCreate() {
    console.log("beforeCreate", this.name);
  },
  created() {
    console.log("created", this.name);
  },

  beforeMount() {
    alert("beforeMount");
  },
  mounted() {
    alert("mounted");
  },

  beforeUpdate() {
    alert("beforeUpdate");
  },
  updated() {
    alert("updated");
  },

  beforeUnmount() {
    alert("beforeUnmount");
  },
  unmounted() {
    alert("unmounted");
  },
  
  methods: {
    updateName() {
      this.name = "hello";
    }
  }
}
</script>


<style scoped lang="scss">
// style scoped lang="scss" : 현재 파일에서만 style 적용시킨다는 뜻
h1 {
  color: red;
}
</style>
