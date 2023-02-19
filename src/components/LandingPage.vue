<template>
    <div class="LandingPageCls">
        <h1>THIS IS A TEST APP</h1>
        <button class="TestButtonCls" @click="test">CLICK ME!</button>
        <body>
            Blah Blah Blah Blah Blah Blah Blah Blah Blah Blah Blah Blah Blah Blah Blah Blah
        </body>
    </div>
</template>

<style scoped>
.LandingPageCls {
    width: 100%;
    height: 10000px;
    background-color: aquamarine;
}

.TestButtonCls {
    background-color: cornflowerblue;
    margin: 10px;
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