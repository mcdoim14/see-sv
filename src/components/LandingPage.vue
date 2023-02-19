<template>
    <div class="LandingPageCls">
        <h1>THIS IS A TEST APP</h1>
        <body>
            Blah Blah Blah Blah Blah Blah Blah Blah Blah Blah Blah Blah Blah Blah Blah Blah
        </body>
        <button @click="test">CLICK ME!</button>
    </div>
</template>

<style scoped>
.LandingPageCls {
    background-color: aquamarine;
}
</style>

<script>

export default {
    data() {
        return {

        }
    },
    methods: {
        test() {
            alert("This is a test alert!");
        }
    }    
}
</script>