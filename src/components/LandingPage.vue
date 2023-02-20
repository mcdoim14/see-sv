<template>
    <NavigationBar></NavigationBar>
    <div class="landing-page">
        <h1>THIS IS A TEST APP</h1>
        <button class="test-button" @click="test">CLICK ME!</button>
        <DxButton
            text="Click me too!"
            @click="sayHelloWorld"
        />
        <Icon>
            <Money16Regular />
        </Icon>
        <!-- Add the style and icon you want using the String format -->
        <body>
            Blah Blah Blah Blah Blah Blah Blah Blah Blah Blah Blah Blah Blah Blah Blah Blah
        </body>
    </div>
</template>

<style scoped>
h1 {
    margin: 0px !important;
}
.nav-bar {
    height: 10%
}
.landing-page {
    width: 100%;
    height: 10000px;
    background-color: rgb(248, 244, 234);
}

.test-button {
    background-color: cornflowerblue;
    margin: 10px;
}
</style>

<script>
import DxButton from 'devextreme-vue/button';
import { Money16Regular } from '@vicons/fluent';
import { Icon } from '@vicons/utils';
import NavigationBar from './NavigationBar';

export default {
    components: {
        DxButton,
        Money16Regular,
        Icon,
        NavigationBar
    },
    data() {
        return {
            
        }
    },
    methods: {
        test() {
            alert("This is a test alert!123");
        },
        sayHelloWorld() {
            alert('Hello world!321');
        }
    }    
}
</script>