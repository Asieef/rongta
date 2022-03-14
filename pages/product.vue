<template>
    <div class="container mx-auto">
        <div class="flex flex-col items-center mt-8">
            <h2 class="text-3xl font-bold uppercase tracking-wider">All Products</h2>

            <img src="/bt-i.png" class="mt-4" />
        </div>

        <div class="grid lg:grid-cols-4 grid-cols-1 gap-6 px-6 py-12" v-if="products != null">
            <div
                class="border-4 border-gray-200 hover:border-rongta"
                v-for="product in products"
                :key="product.slug"
            >
                <router-link :to="`/product/${product.slug}`">
                    <img :src="product.thumbnail" alt="Casing" style="width:250px" />
                    <p class="text-rongtatext text-sm font-semibold px-8 py-2">{{ product.name }}</p>
                </router-link>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            products: [],
            category: "thermal-printer",
            cat_id: [57],
        };
    },

    mounted() {
        this.getData();
    },
    methods: {
        getData() {
            this.$axios
                .get("https://admindash.comcitybd.com/api/brands/Rongta/20", {
                    params: {
                        id: this.cat_id,
                    },
                })
                .then((response) => {
                    console.log(response.data);
                    this.products = response.data.data;
                });
        },
    },
};
</script>

