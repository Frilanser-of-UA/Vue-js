<template>
    <a :href="product.link" class="product-card">
        <img :src="product.image" :alt="product.name" />
        <h3>{{ product.name }}</h3>
        <p class="price">
            <span v-if="product.oldPrice" class="old-price"
                >{{ product.oldPrice }} ₴</span
            >
            <span>{{ product.price }} ₴</span>
        </p>
        <p v-if="product.inStock" class="in-stock">Є в наявності</p>
        <p v-else class="out-of-stock">Немає в наявності</p>
    </a>
</template>
  
  <script>
export default {
    props: {
        product: {
            type: Object,
            required: true,
        },
    },
};
</script>
  
  <style scoped>
.product-card {
    border: 1px solid #ddd;
    padding: 10px;
    text-align: center;
    width: 180px;
}
img {
    width: 100%;
}
.old-price {
    text-decoration: line-through;
    color: red;
}
.in-stock {
    color: green;
}
.out-of-stock {
    color: red;
}
</style>
  