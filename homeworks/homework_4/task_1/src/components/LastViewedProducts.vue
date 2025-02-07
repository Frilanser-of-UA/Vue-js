<template>
    <div>
        <h2>Останні переглянуті товари</h2>
        <div class="row g-2">
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
        products: {
            type: Array,
            required: true,
        },
    },
};
</script>
  
  <style scoped>
</style>
  