<template>
    <div class="container mx-auto">
        <div class="flex flex-col items-center mt-8">
            <h2 class="text-3xl font-bold uppercase tracking-wider">Faq</h2>

            <img src="/bt-i.png" class="mt-4" />
        </div>

        <div class="px-12 mt-8">
            <!-- FAQ 1 -->
            <h2
                class="font-semibold text-lg text-rongtatext py-4 cursor-pointer"
                @click="toggleFaqOne"
            >Who is authorized distributor of rongta in Bangladesh?</h2>

            <transition
                enter-active-class="transition ease-out duration-300"
                enter-class="transform opacity-0 scale-95"
                enter-to-class="transform opacity-100 scale-100"
                leave-active-class="transition ease-in duration-75"
                leave-class="transform opacity-100 scale-100"
                leave-to-class="transform opacity-0 scale-95"
            >
                <h2
                    class="font-semibold text-gray-700 py-4"
                    v-if="showFaqOne"
                >- Computer City Technologies Limited is the authorized distributor of Rongta in Bangladesh.</h2>
            </transition>

            <!-- FAQ 2 -->
            <h2
                class="font-semibold text-lg text-rongtatext py-4 cursor-pointer"
                @click="toggleFaqTwo"
            >How to Purchase from distributor?</h2>

            <transition
                enter-active-class="transition ease-out duration-300"
                enter-class="transform opacity-0 scale-95"
                enter-to-class="transform opacity-100 scale-100"
                leave-active-class="transition ease-in duration-75"
                leave-class="transform opacity-100 scale-100"
                leave-to-class="transform opacity-0 scale-95"
            >
                <h2
                    class="font-semibold text-gray-700 py-4"
                    v-if="showFaqTwo"
                >- - Contact 01938 858802</h2>
            </transition>

            <!-- FAQ 3 -->
            <h2
                class="font-semibold text-lg text-rongtatext py-4 cursor-pointer"
                @click="toggleFaqThree"
            >Does Rongta products have warranty?</h2>

            <transition
                enter-active-class="transition ease-out duration-300"
                enter-class="transform opacity-0 scale-95"
                enter-to-class="transform opacity-100 scale-100"
                leave-active-class="transition ease-in duration-75"
                leave-class="transform opacity-100 scale-100"
                leave-to-class="transform opacity-0 scale-95"
            >
                <h2
                    class="font-semibold text-gray-700 py-4"
                    v-if="showFaqThree"
                >- - Yes, Rongta products have 1 year standard warrranty</h2>
            </transition>
        </div>
    </div>
</template>

<script>

export default {
    data() {
        return {
            showFaqOne: false,
            showFaqTwo: false,
            showFaqThree: false,

        }
    },

    methods: {
        toggleFaqOne() {
            this.showFaqOne = !this.showFaqOne
        },

        toggleFaqTwo() {
            this.showFaqTwo = !this.showFaqTwo
        },

        toggleFaqThree() {
            this.showFaqThree = !this.showFaqThree
        },

    },

    head: {
        title: 'Rongta Bangladesh | FAQs',
        meta: [
            { charset: 'utf-8' },
            { name: 'viewport', content: 'width=device-width, initial-scale=1' },
            {
                hid: 'description',
                name: 'Frequently Asked Questions',
                content: 'Point of Sales Solution in Bangladesh'
            }
        ],
        link: [{ rel: 'icon', type: 'image/x-icon', href: '/fav.png' }]
    },
}

</script>