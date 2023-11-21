<template>
    <div>
        <!-- <h1>title</h1> -->
        <h1>{{ title }}</h1>
        <h2>{{ age }}</h2>
        <p>{{ name }}</p>
        <br>
        <button @click="updateName">update name</button>
    </div>
</template>

<script>
export default {
    name: "KossieCoder",
    // props: [
    //     "title"
    // ],
    props: {
        title: {
            type: String, // 해당 타입만 사용 가능
            required: false, // true: props 무조건 사용, false: 사용해도 사용안해도 상관없음
            default: "default title"
        },
        age: {
            type: String,
            default: "default age"
        }
    },
    data() {
        return {
            name: "Kossie Coder"
        }
    },
    methods: {
        updateName() {
            this.name = "Kossie Coder Updated";
        }
    }
}
</script>

<style>

</style>