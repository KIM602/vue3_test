<template>
    <div
        class="parent"
        @click.self="handlerA">
        <div
            class="child"></div>
    </div>
</template>

<script>
export default {
    methods: {
        handlerA() {
            console.log('A')
        },
        handlerB(event) {
            event.stopPropagation()
            console.log('B')
        }
    }
}
</Script>

<style scoped lang="scss">
    .parent {
        width: 200px;
        height: 100px;
        background-color: royalblue;
        margin: 10px;
        padding: 10px;
        .child {
            width: 100px;
            height: 100px;
            background-color: orange;
        }
    }
</style>