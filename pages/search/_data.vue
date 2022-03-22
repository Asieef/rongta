<template>
    <div class="container mx-auto">
        <h3 class="px-6 font-semibold uppercase mt-8">Search Result For "{{ query }}"</h3>

        <div class="grid lg:grid-cols-4 grid-cols-1 gap-6 px-6 py-12" v-if="products != null">
            <div
                class="border-4 border-gray-200 hover:border-rongta"
                v-for="product in products"
                :key="product.slug"
            >
                <nuxt-link :to="`/product/${product.slug}`">
                    <img :src="product.thumbnail" alt="Casing" style="width:250px" />
                    <p class="text-rongtatext text-sm font-semibold px-8 py-2">{{ product.name }}</p>
                </nuxt-link>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            query: this.$route.params.data,
            products: [],
        };
    },

    watch: {
        "$route.params.data"(newSlug) {
            this.getData(newSlug);
        },
    },

    mounted() {
        this.getData(this.query);
    },

    methods: {
        getData(newSlug) {
            this.query = newSlug;
            this.$axios
                .get(`https://admindash.comcitybd.com/api/customsearch/Rongta/${this.query}`)
                .then((response) => {
                    console.log(response.data);
                    this.products = response.data.data;
                });
        },
    },
};
</script>