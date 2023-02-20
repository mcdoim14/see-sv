<template>
    <div class="form nav-bar">
        <div>
            <div class="label">Catalog:</div>
            <DxMenu
                :data-source="products"
                :show-first-submenu-mode="showFirstSubmenuModes"
                :orientation="orientation"
                :hide-submenu-on-mouse-leave="hideSubmenuOnMouseLeave"
                display-expr="name"
                @item-click="itemClick"
            />
            <div v-if="currentProduct" id="product-details">
                <!-- <img :src="currentProduct.icon"> -->
                <div class="name">{{ currentProduct.name }}</div>
                <div class="price">{{ "$" + currentProduct.price }}</div>
            </div>
        </div>
  </div>
</template>

<style scoped>
.nav-bar {
    background-color: rgb(87, 155, 177);
}

.form {
  margin-left: 3px;
}

.form > div:first-child {
  margin-right: 320px;
}

.label {
  font-size: 22px;
}

#product-details {
  width: 400px;
  height: 400px;
  margin: 20px auto 0;
}

#product-details > img {
  height: 300px;
  width: 400px;
}

#product-details > .name {
  text-align: center;
  font-size: 20px;
}

#product-details > .price {
  text-align: center;
  font-size: 24px;
}

.dark #product-details > div {
  color: #f0f0f0;
}

.options {
  padding: 20px;
  position: absolute;
  bottom: 0;
  right: 0;
  width: 260px;
  top: 0;
  background-color: rgba(191, 191, 191, 0.15);
}

.caption {
  font-size: 18px;
  font-weight: 500;
}

.option {
  margin-top: 10px;
}

.hidden {
  visibility: hidden;
}
</style>

<script>
import DxMenu from 'devextreme-vue/menu';

export default {
    props: {
        color: String,
        height: String,
        width: String,
    },
    components: {
        DxMenu,
    },
    created() {
        // if(this.color == null) {
        //     this.color = "#FFFFFF";
        // }
        // if(this.height == null) {
        //     this.height = "10%";
        // }
        // if(this.width == null) {
        //     this.width = "100%";
        // }
    }, 
    data() {
        const products = [{
            id: '1',
            name: 'Video Players',
            items: [{
                id: '1_1',
                name: 'HD Video Player',
                price: 220,
            }, {
                id: '1_2',
                name: 'SuperHD Video Player',
                price: 270,
            }],
            }, {
            id: '2',
            name: 'Televisions',
            items: [{
                id: '2_1',
                name: 'SuperLCD 42',
                price: 1200,
            }, {
                id: '2_2',
                name: 'SuperLED 42',
                price: 1450,
            }, {
                id: '2_3',
                name: 'SuperLED 50',
                price: 1600,
            }, {
                id: '2_4',
                name: 'SuperLCD 55 (Not available)',
                price: 1350,
                disabled: true,
            }, {
                id: '2_5',
                name: 'SuperLCD 70',
                price: 4000,
            }],
            }, {
            id: '3',
            name: 'Monitors',
            items: [{
                id: '3_1',
                name: '19"',
                items: [{
                id: '3_1_1',
                name: 'DesktopLCD 19',
                price: 160,
                }],
            }, {
                id: '3_2',
                name: '21"',
                items: [{
                id: '3_2_1',
                name: 'DesktopLCD 21',
                price: 170,
                }, {
                id: '3_2_2',
                name: 'DesktopLED 21',
                price: 175,
                }],
            }],
            }, {
            id: '4',
            name: 'Projectors',
            items: [{
                id: '4_1',
                name: 'Projector Plus',
                price: 550,
            }, {
                id: '4_2',
                name: 'Projector PlusHD',
                price: 750,
            }],
            }];
        const showSubmenuModes = [{
            name: 'onHover',
            delay: { show: 0, hide: 500 },
        },
        {
            name: 'onClick',
            delay: { show: 0, hide: 300 },
        }];
        return {
            products,
            showSubmenuModes,
            showFirstSubmenuModes: showSubmenuModes[1],
            orientation: 'horizontal',
            hideSubmenuOnMouseLeave: false,
            currentProduct: null,
        };
    },
    methods: {
        itemClick(e) {
            if (e.itemData.price) {
                this.currentProduct = e.itemData;
            }
        },
    }
}
</script>