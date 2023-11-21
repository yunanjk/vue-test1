<template>
  <div>
    <h1>This is home page</h1>
    <form action="">
      <!-- <label for="">Name</label>
      <input type="text" v-model="name" style="margin: 10px; padding: 20px; border: 3px solid green;">-->
      <InputField :name="name" @update-name="updateName"/>
      <button>submit</button>
    </form>
    {{ name }}
  </div>
</template>

<script>
import InputField from "@/components/InputField.vue";

export default {
  name: 'HomeView',
  data() {
    return {
      name: ""
    }
  },
  methods: {
    updateName(name) {
      this.name = name;
    }
  },
  components: {
    InputField
  }
}
</script>


<style scoped lang="scss">
// style scoped lang="scss" : 현재 파일에서만 style 적용시킨다는 뜻
h1 {
  color: red;
}
</style>
