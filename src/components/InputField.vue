<template>
    <div>
        <label for="">Name</label>
        <input 
            type="text" 
            :value="name" 
            style="margin: 10px; padding: 20px; border: 3px solid green;"
            @input="updateName"
        >
    </div>
</template>

<script>
export default {
    props: {
        name: {
            type: String,
            required: true
        }
    },
    methods: {
        updateName(event) {
            // console.log(event.target.value);
            this.$emit("update-name", event.target.value);
        }
    }
}
</script>