<template>
    <NavigationBar></NavigationBar>
    <div class="landing-page">
        <div id="navPanelButton" class="left-side-panel">
            <NavigationPane></NavigationPane>
        </div>
        <div id="navPlaceholder" class="top-bar">
            <div>TEST</div>
        </div>
        <!-- <button class="test-button" @click="test">CLICK ME!</button>
        <DxButton text="Click me too!" @click="sayHelloWorld"/> -->
        <!-- <Icon>
            <Money16Regular />
        </Icon> -->
        <!-- Add the style and icon you want using the String format -->
    </div>
</template>

<style scoped>
#navPanelButton {
    z-index: 10;
    position: relative;
}

#navPlaceholder {
    position: absolute;
}

.nav-bar {
    height: 10%
}

.top-bar {
    background-color: rgb(236 190 110);
    float: right;
    width: 100vw;
    height: 46px;
}
.left-side-panel {
    /* display: flex; */
    float: left;
}

h1 {
    margin: 0px !important;
}

.landing-page {
    /* display: flex; */
    /* flex-direction: column; */
    width: 100%;
    height: 10000px;
    background-color: rgb(248, 244, 234);
    position: relative;
}

.test-button {
    background-color: cornflowerblue;
    margin: 10px;
}
</style>

<script>
// import DxButton from 'devextreme-vue/button';
// import { Money16Regular } from '@vicons/fluent';
// import { Icon } from '@vicons/utils';
import NavigationBar from './NavigationBar';
import NavigationPane from './NavigationPane';

export default {
    components: {
        // DxButton,
        // Money16Regular,
        // Icon,
        NavigationBar,
        NavigationPane
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