<template>
    <div class="nav-bar">
        <!-- <Icon>
            <Settings16Regular></Settings16Regular>
        </Icon> -->
    </div>
</template>

<style scoped>
.nav-tabs {
    position: absolute;
    /* align-self: bottom; */
}
.nav-bar {
    background-color: rgb(87, 155, 177);
    align-items: baseline;
}
</style>

<script>
// import { Icon } from '@vicons/utils';
// import { Settings16Regular } from '@vicons/fluent';

export default {
    props: {
        color: String,
        height: String,
        width: String,
    },
    components: {
    // Settings16Regular,
    // Icon,
},
    created() {
        
    }, 
    data() {
        return {
            selectedIndex: 0,
        };
    },
    methods: {
        
    }
}
</script>