<template>
    <div class="comparison-list">
        <h2>Списки порівнянь</h2>
        <div class="category">
            <h3>Мобільні телефони</h3>
            <p>Кількість товарів: {{ products.length }}</p>
            <div class="phones">
                <img
                    v-for="phone in products"
                    :key="phone.id"
                    :src="phone.image"
                    alt="Phone"
                />
            </div>
        </div>
    </div>
</template>
  
  <script>
export default {
    props: {
        products: {
            type: Array,
            required: true,
        },
    },
};
</script>
  
  <style scoped>
.comparison-list {
    margin-bottom: 20px;
}
.phones img {
    width: 100px;
    margin-right: 15px;
}
</style>
  