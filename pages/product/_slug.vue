<template>
    <div>
        <div class="spin-container" v-if="loading">
            <div class="lds-facebook">
                <div></div>
                <div></div>
                <div></div>
            </div>
        </div>

        <div class="container mx-auto">
            <div class="grid lg:grid-flow-col lg:grid-cols-2 grid-cols-1 gap-6 p-16">
                <div class="col-span-1 border border-gray-200">
                    <img :src="product.photo" :alt="product.name" style="width: 100%" />
                </div>

                <div class="col-span-1">
                    <h2 class="font-bold text-2xl text-rongtatext">{{ product.name }}</h2>
                    <p class="font-semibold text-rongtatext mt-6" v-html="product.short"></p>
                </div>
            </div>
        </div>

        <div class="bg-gray-800 text-white font-semibold uppercase flex justify-center px-4 py-4">
            <div class="px-8">
                <button
                    @click="selectTab(1)"
                    :class="{ tabstate: currentTab == 1 }"
                    class="tab"
                >Description</button>
            </div>

            <div class="px-8">
                <button
                    @click="selectTab(2)"
                    :class="{ tabstate: currentTab == 2 }"
                    class="tab"
                >Specification</button>
            </div>
        </div>

        <div class="px-8 container mx-auto">
            <div v-if="currentTab == 1" class="tabpanel">
                <div class="px-10 py-6" v-html="product.details"></div>
            </div>

            <div v-if="currentTab == 2" class="tabpanel">
                <div class="px-10 py-6" v-html="product.short"></div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    props: {
        value: String,
    },

    data() {
        return {
            product: [],
            slug: this.$route.params.slug,
            currentTab: 1,
            loading: false,
        };
    },

    head() {
        return {
            title: `Rongta | ${this.slug}`,
            meta: [
                {
                    hid: "description",
                    name: "description",
                    content: "Home page description",
                },
            ],
        };
    },

    mounted() {
        this.getProduct();
        console.log(this.slug);
    },

    methods: {
        getProduct() {
            this.loading = true;
            this.$axios
                .get(`https://admindash.comcitybd.com/api/product/${this.slug}`)
                .then((response) => {
                    this.loading = false;
                    console.log(response.data);
                    this.product = response.data;
                });
        },

        selectTab(selectedTab) {
            this.currentTab = selectedTab;
        },
    },
};
</script>

<style>
.tabstate {
    border-bottom: 3px solid #f08200;
}
</style>