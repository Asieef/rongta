<template>
    <div>
        <Header class="hidden lg:block" @custom-search="searchs" />
        <Mobilenav class="block lg:hidden" />
        <Nuxt />
        <Footer />
    </div>
</template>



<script>
export default {
    data() {
        return {
            showSearch: false,
            mydata: "",
        };
    },
    created() {
        this.$nuxt.$on("customSearch", ($event) => this.searchs($event));
    },
    methods: {
        searchs(event) {
            console.log(event);
            this.$router.push({ path: `/search/${event}` });
        },

        test(e) {
            console.log(e);
        },
    },
};
</script>