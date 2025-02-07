<template>
    <div class="container">
        <ComparisonList :products="comparisonProducts" />
        <LastViewedProducts :products="viewedProducts" />
    </div>
</template>
  
  <script>
import ComparisonList from "./components/ComparisonList.vue";
import LastViewedProducts from "./components/LastViewedProducts.vue";

export default {
    components: {
        ComparisonList,
        LastViewedProducts,
    },
    data() {
        return {
            comparisonProducts: [
                {
                    id: 1,
                    image: "https://content2.rozetka.com.ua/goods/images/big_tile/507063004.jpg",
                },
                {
                    id: 2,
                    image: "https://content2.rozetka.com.ua/goods/images/big_tile/468888082.jpg",
                },
                {
                    id: 3,
                    image: "https://content.rozetka.com.ua/goods/images/big_tile/505511671.jpg",
                },
            ],
            viewedProducts: [
                {
                    id: 1,
                    name: "Портативний екран TouYinger 130",
                    price: 1899,
                    image: "https://content1.rozetka.com.ua/goods/images/big/443160732.jpg",
                    inStock: true,
                    link: "https://rozetka.com.ua/420151755/p420151755/",
                },
                {
                    id: 2,
                    name: "Портативний монітор MUCAI N116A",
                    price: 2950,
                    image: "https://content2.rozetka.com.ua/goods/images/big/478831788.jpg",
                    inStock: true,
                    link: "https://hard.rozetka.com.ua/453448043/p453448043/",
                },
                {
                    id: 3,
                    name: "Шафа розпашна Roko Дуб Венге",
                    oldPrice: 3504,
                    price: 2976,
                    image: "https://content1.rozetka.com.ua/goods/images/big/341037293.jpg",
                    inStock: false,
                    link: "https://rozetka.com.ua/roko-20200047514/p382070007/",
                },
            ],
        };
    },
};
</script>
  