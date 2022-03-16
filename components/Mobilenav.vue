<template>
    <div>
        <div class="grid grid-flow-col grid-cols-2 relative p-4">
            <div>
                <div class="col-span-1 flex items-center justify-start">
                    <NuxtLink to="/">
                        <img src="/logo.png" class="w-20" />
                    </NuxtLink>
                </div>
            </div>

            <div class="col-span-1 flex justify-end items-center">
                <div class="px-3" @click="toggleSearch">
                    <img src="/search.svg" class="w-5" />
                </div>

                <div class="px-3" @click="toggleMenu">
                    <img src="/ham.png" class="w-5" />
                </div>
            </div>
            <transition
                enter-active-class="transition ease-out duration-300"
                enter-class="transform opacity-0 scale-95"
                enter-to-class="transform opacity-100 scale-100"
                leave-active-class="transition ease-in duration-200"
                leave-class="transform opacity-100 scale-100"
                leave-to-class="transform opacity-0 scale-95"
            >
                <div
                    class="w-[180px] grid grid-flow-col grid-cols-8 gap-1 absolute bottom-0 right-8"
                    v-if="showSearch"
                >
                    <div class="col-span-6 border-0 bg-white text-rongtatext">
                        <input type="text" class="border border-slate-400" />
                    </div>

                    <div
                        class="col-span-1 flex justify-center items-center bg-rongta hover:bg-gray-200"
                    >
                        <img src="/search.svg" class="w-4" />
                    </div>

                    <div
                        class="col-span-1 flex justify-center items-center bg-rongta hover:bg-gray-200 cursor-pointer"
                        @click="toggleSearch"
                    >
                        <img src="/close.svg" class="w-2" />
                    </div>
                </div>
            </transition>

            <transition
                enter-active-class="transition ease-out duration-300"
                enter-class="transform opacity-0 scale-95"
                enter-to-class="transform opacity-100 scale-100"
                leave-active-class="transition ease-in duration-200"
                leave-class="transform opacity-100 scale-100"
                leave-to-class="transform opacity-0 scale-95"
            >
                <div class="absolute bg-white top-20 left-0 w-full" v-if="showMenu">
                    <ul class="uppercase">
                        <li class="px-2 py-2 border-b text-sm font-bold border-slate-100">
                            <NuxtLink class="hover:text-rongta" to="/">Home</NuxtLink>
                        </li>
                        <li class="px-2 py-2 block border-b text-sm font-bold border-slate-100">
                            <NuxtLink class="hover:text-rongta" to="/about">About Us</NuxtLink>
                        </li>
                        <li class="px-2 py-2 border-b block text-sm font-bold border-slate-100">
                            <NuxtLink class="hover:text-rongta" to="/">Products</NuxtLink>
                        </li>
                        <li class="px-2 py-2 border-b block text-sm font-bold border-slate-100">
                            <NuxtLink class="hover:text-rongta" to="/">Solution</NuxtLink>
                        </li>
                        <li class="px-2 py-2 block text-sm font-bold">
                            <NuxtLink class="hover:text-rongta" to="/">Contact Us</NuxtLink>
                        </li>
                    </ul>
                </div>
            </transition>
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            showSearch: false,
            showMenu: false
        }
    },

    methods: {
        toggleSearch() {
            this.showSearch = !this.showSearch
        },

        toggleMenu() {
            this.showMenu = !this.showMenu
        }
    }
}
</script>