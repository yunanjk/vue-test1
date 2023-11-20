<template>
    <div>
        <p>{{ name }}</p>
        <br>
        <button @click="updateName">update name</button>
    </div>
</template>

<script>
export default {
    name: "KossieCoder",
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