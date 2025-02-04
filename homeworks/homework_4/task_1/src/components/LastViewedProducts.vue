<template>
    <div class="last-viewed">
        <h2>Останні переглянуті товари</h2>
        <div class="products">
            <ProductCard
                v-for="product in products"
                :key="product.id"
                :product="product"
            />
        </div>
    </div>
</template>
  
  <script>
import ProductCard from "./ProductCard.vue";

export default {
    components: {
        ProductCard,
    },
    props: {
        products: Array,
    },
};
</script>
  
  <style scoped>
.products {
    display: flex;
    gap: 10px;
    overflow-x: auto;
}
</style>
  