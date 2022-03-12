<template>
    <div>
        <div
            style="background-image: url('/category-bg.jpg')"
            class="h-[680px] bg-cover bg-no-repeat bg-top bg-fixed"
        >
            <div class="grid grid-flow-row py-16 px-8">
                <div class="flex flex-col items-center">
                    <h2 class="text-3xl font-bold uppercase tracking-wider">Product Category</h2>

                    <img src="/bt-i.png" class="mt-4" />
                </div>

                <div>
                    <div class="grid grid-flow-col grid-cols-4 gap-4 mt-16">
                        <a href="#">
                            <div
                                style="background-image: url('/receipt-printer.jpg')"
                                class="col-span-1 h-[400px] bg-cover bg-no-repeat bg-center hover:brightness-75"
                            >
                                <h2
                                    class="text-white font-bold uppercase p-2 text-lg tracking-wider"
                                >Receipt Printer</h2>
                            </div>
                        </a>

                        <a href="#">
                            <div
                                style="background-image: url('/mobile-printer.jpg')"
                                class="col-span-1 h-[400px] bg-cover bg-no-repeat bg-center hover:brightness-75"
                            >
                                <h2
                                    class="text-white font-bold uppercase p-2 text-lg tracking-wider"
                                >Mobile Printer</h2>
                            </div>
                        </a>

                        <a href="#">
                            <div
                                style="background-image: url('/lable-printer.jpg')"
                                class="col-span-1 h-[400px] bg-cover bg-no-repeat bg-center hover:brightness-75"
                            >
                                <h2
                                    class="text-white font-bold uppercase p-2 text-lg tracking-wider"
                                >Label Printer</h2>
                            </div>
                        </a>

                        <a href="#">
                            <div
                                style="background-image: url('/cash-drawer.jpg')"
                                class="col-span-1 h-[400px] bg-cover bg-no-repeat bg-center hover:brightness-75"
                            >
                                <h2
                                    class="text-white font-bold uppercase p-2 text-lg tracking-wider"
                                >Cash Drawer</h2>
                            </div>
                        </a>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>