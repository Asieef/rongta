<template>
    <div>
        <div
            style="background-image: url('/about-bg.jpg')"
            class="h-[600px] bg-cover bg-no-repeat bg-center bg-fixed grid lg:grid-flow-col lg:grid-cols-2 grid-cols-1"
        >
            <div class="lg:col-span-1 lg:flex lg:justify-center lg:items-center lg:ml-8 hidden">
                <div class="bg-white py-16 px-12 shadow">
                    <h2 class="text-lg font-semibold">Rongta Technology (Xiamen) Group Co.,Ltd.</h2>
                    <p class="text-rongtatext text-sm mt-8 mb-6">
                        Rongta Technology (Xiamen) Group Co., Ltd. is a high-tech enterprise established in Jan 1st, 2009, specializing in R&D, manufacturing and marketing of pos printers, receipt printers, label scales, thermal transfer barcode printers, impact printers, printer mechanism, control boards and other POS peripherals.
                        <br />
                        <br />Computer City Technologies Ltd. is the authorized distributor for Rongta in Bangladesh
                    </p>

                    <NuxtLink
                        class="text-white bg-rongta px-8 py-2 uppercase text-sm hover:bg-rongtatext"
                        to="/about"
                    >Read More</NuxtLink>
                </div>
            </div>

            <div class="col-span-1">
                <div class="bg-rongta opacity-95 h-full grid grid-flow-row">
                    <div class="flex justify-end flex-col px-12">
                        <h2 class="text-white uppercase text-3xl font-bold">About Rongta</h2>
                        <img src="/line.png" class="w-16" />
                    </div>
                    <div class="grid grid-flow-col grid-cols-2 justify-items-center">
                        <div class="col-span-1 flex flex-col gap-12">
                            <div class="flex gap-4">
                                <div
                                    class="border border-white rounded flex items-center justify-center w-20 h-20"
                                >
                                    <img src="/calendar.png" class="lg:w-12 w-8" />
                                </div>
                                <div class="uppercase text-white">
                                    <h2 class="font-bold lg:text-4xl text-lg">2009</h2>
                                    <p class="lg:text-sm text-xs py-2">established</p>
                                </div>
                            </div>

                            <div class="flex gap-4">
                                <div
                                    class="border border-white rounded flex items-center justify-center w-20 h-20"
                                >
                                    <img src="/flag.png" class="lg:w-12 w-8" />
                                </div>
                                <div class="uppercase text-white">
                                    <h2 class="font-bold lg:text-4xl text-lg">5000+</h2>
                                    <p class="lg:text-sm text-xs py-2">Distributors</p>
                                </div>
                            </div>
                        </div>

                        <div class="col-span-1 flex flex-col gap-12">
                            <div class="flex gap-4">
                                <div
                                    class="border border-white rounded flex items-center justify-center w-20 h-20"
                                >
                                    <img src="/building.png" class="lg:w-12 w-8" />
                                </div>
                                <div class="uppercase text-white">
                                    <h2 class="font-bold lg:text-4xl text-lg">20000+</h2>
                                    <p class="lg:text-sm text-xs py-2">Company Area</p>
                                </div>
                            </div>

                            <div class="flex gap-4">
                                <div
                                    class="border border-white rounded flex items-center justify-center w-20 h-20"
                                >
                                    <img src="/user.png" class="lg:w-12 w-8" />
                                </div>
                                <div class="uppercase text-white">
                                    <h2 class="font-bold lg:text-4xl text-lg">600+</h2>
                                    <p class="lg:text-sm text-xs py-2">Customers (Mil)</p>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>