<template>
    <div>
        <div class="grid grid-cols-12 shadow-md h-24 px-8 relative">
            <div class="col-span-4 flex items-center justify-start">
                <img src="/logo.png" class="w-20" />
            </div>

            <div class="col-span-8 flex items-center justify-end">
                <ul class="uppercase text-[#333] font-bold">
                    <li class="inline-block px-3">
                        <a
                            href="#"
                            class="py-2 hover:text-rongta hover:border-b-2 hover:border-rongta"
                        >Home</a>
                    </li>
                    <li class="inline-block px-3">
                        <a
                            href="#"
                            class="py-2 hover:text-rongta hover:border-b-2 hover:border-rongta"
                        >About Us</a>
                    </li>

                    <li class="inline-block px-3">
                        <a
                            href="#"
                            class="py-2 hover:text-rongta hover:border-b-2 hover:border-rongta"
                        >Products</a>
                    </li>

                    <li class="inline-block px-3">
                        <a
                            href="#"
                            class="py-2 hover:text-rongta hover:border-b-2 hover:border-rongta"
                        >Solution</a>
                    </li>

                    <li class="inline-block px-3">
                        <a
                            href="#"
                            class="py-2 hover:text-rongta hover:border-b-2 hover:border-rongta"
                        >Contact Us</a>
                    </li>

                    <li class="inline-block px-3" @click="toggleSearch">
                        <a href="#" class="hover:text-rongta hover:border-b-2 hover:border-rongta">
                            <img src="/search.svg" class="w-4" />
                        </a>
                    </li>
                </ul>
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
                    class="w-[240px] grid grid-flow-col grid-cols-8 gap-1 absolute bottom-2 right-10"
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
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            showSearch: false
        }
    },

    methods: {
        toggleSearch() {
            this.showSearch = !this.showSearch
        }
    }
}
</script>