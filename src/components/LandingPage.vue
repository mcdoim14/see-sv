<template>
    <div class="LandingPageCls">
        <h1>THIS IS A TEST APP</h1>
        <button class="TestButtonCls" @click="test">CLICK ME!</button>
        <DxButton
            text="Click me too!"
            @click="sayHelloWorld"
        />
        <DxChart
            :data-source="data">
            <DxArgumentAxis :tick-interval="10" />
            <DxSeries type="bar" />
            <DxLegend :visible="false" />
        </DxChart>
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
import DxButton from 'devextreme-vue/button';
import DxChart, { DxArgumentAxis, DxSeries, DxLegend } from 'devextreme-vue/chart';

const data = [{
    arg: 1990,
    val: 5320816667
}, {
    arg: 2000,
    val: 6127700428
}, {
    arg: 2010,
    val: 6916183482
}];

export default {
    components: {
        DxButton,
        DxChart,
        DxArgumentAxis,
        DxSeries,
        DxLegend
    },
    data() {
        return {
            data,
        }
    },
    methods: {
        test() {
            alert("This is a test alert!");
        },
        sayHelloWorld() {
            alert('Hello world!');
        }
    }    
}
</script>