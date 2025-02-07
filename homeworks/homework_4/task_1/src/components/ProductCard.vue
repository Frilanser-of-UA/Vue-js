<template>
    <div class="col-4">
        <a :href="product.link" class="card text-decoration-none">
            <div class="p-3">
                <img :src="product.image" :alt="product.name" />
            </div>
            <div class="card-body p-2 text-body">
                <h3 class="h6">{{ product.name }}</h3>
                <div class="d-flex gap-2">
                    <div v-if="product.oldPrice" class="old-price">
                        {{ product.oldPrice }} ₴
                    </div>
                    <div>{{ product.price }} ₴</div>
                </div>
                <p v-if="product.inStock" class="in-stock">Є в наявності</p>
                <p v-else class="out-of-stock">Немає в наявності</p>
            </div>
        </a>
    </div>
</template>
  
  <script>
export default {
    props: {
        product: {
            type: Object,
            default: () => ({}),
        },
    },
};
</script>
  
  <style scoped>
img {
    width: 100%;
    height: 200px;
    object-fit: cover;
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
  