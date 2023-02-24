<template>
    <div style="width: 20vw;">
        <DxList
        :data-source="navigation"
        :active-state-enabled="false"
        :hover-state-enabled="false"
        :focus-state-enabled="false"
        class="panel-list dx-theme-accent-as-background-color"
        />
    </div>
</template>

<style scoped>

</style>

  <script>
  import { DxList } from 'devextreme-vue/list';
  
  export default {
    components: {
      DxList,
    },
    data() {
        const navigation = [
            { id: 1, text: 'Products', icon: 'product' },
            { id: 2, text: 'Sales', icon: 'money' },
            { id: 3, text: 'Customers', icon: 'group' },
            { id: 4, text: 'Employees', icon: 'card' },
            { id: 5, text: 'Reports', icon: 'chart' },
        ];
      return {
        navigation,
      };
    },
  };
  </script>