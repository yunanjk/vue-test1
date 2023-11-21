<template>
    <div>
        <h3>HEADER</h3>
        <!-- 부모 컴포넌트로 데이터를 보낼때 :kossie="kossie"에서 ':kossie'라고 속성명을 지정하고 data값 넘기면 됨 -->
        <slot name="header" :kossie="kossie"></slot>
        <h3>BODY</h3>
        <slot></slot>
        <h3>FOOTER</h3>
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
            name: "Kossie Coder",
            kossie: "coder"
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