<template>
    <div>
        <div
            style="background-image: url('/footer-bg.jpg')"
            class="h-[480px] bg-cover bg-no-repeat bg-center bg-fixed grid grid-flow-row"
        >
            <!-- Newsletter Section -->
            <div class="mt-8 px-8">
                <div
                    class="grid lg:grid-flow-col lg:grid-cols-10 grid-cols-1 gap-4 justify-items-center"
                >
                    <div class="flex gap-4 col-span-4 items-center">
                        <div>
                            <img src="/mail.png" class="w-16" />
                        </div>
                        <div>
                            <h2 class="text-lg text-white uppercase font-bold">Sign up for Newletter</h2>
                            <p
                                class="text-xs text-gray-300"
                            >Wants To Get Latest Updates! Sign Up For Free</p>
                        </div>
                    </div>

                    <div class="col-span-2 flex justify-end items-center">
                        <img src="/facebook.png" class="w-8" />
                    </div>

                    <div class="col-span-4 flex justify-center items-center">
                        <div>
                            <input
                                type="text"
                                value="Enter your email address"
                                class="lg:w-80 w-64 h-12 px-4"
                            />
                        </div>
                        <div class="bg-white h-12 flex items-center px-2">
                            <div>
                                <a
                                    href="#"
                                    class="text-white bg-rongta px-8 py-2 uppercase text-sm hover:bg-rongtatext"
                                >Submit</a>
                            </div>
                        </div>
                    </div>
                </div>
            </div>

            <div class="border-t border-gray-600"></div>

            <!-- Links Section -->

            <div class="grid lg:grid-flow-col lg:grid-cols-4 gap-4 justify-items-center px-8">
                <div class="col-span-1">
                    <ul>
                        <li class="text-white uppercase py-2 text-xl font-semibold">Contact Us</li>
                        <li
                            class="text-sm text-gray-400 py-2"
                        >75-76, B.S. Bhaban, 3rd Floor Laboratory Road Dhaka-1205, Bangladesh</li>
                        <li class="text-sm text-gray-400 py-2">Tel:+880 2 9612629-30</li>
                        <li class="text-sm text-gray-400 py-2">info AT rongta.com.bd</li>
                    </ul>
                </div>

                <div class="col-span-1 lg:block hidden">
                    <ul>
                        <li
                            class="text-white uppercase py-2 text-xl font-semibold"
                        >Service & Support</li>
                        <li class="text-sm text-gray-400 py-2">Privacy Policy</li>
                        <li class="text-sm text-gray-400 py-2">User Manual</li>
                        <li class="text-sm text-gray-400 py-2">Driver Download</li>
                        <li class="text-sm text-gray-400 py-2">FAQ</li>
                    </ul>
                </div>

                <div class="col-span-1 lg:block hidden">
                    <ul>
                        <li class="text-white uppercase py-2 text-xl font-semibold">New Products</li>
                        <li class="text-sm text-gray-400 py-2">RP327-UP</li>
                        <li class="text-sm text-gray-400 py-2">RP328-UP</li>
                        <li class="text-sm text-gray-400 py-2">RP328-UW</li>
                    </ul>
                </div>

                <div class="col-span-1 lg:block hidden">
                    <ul>
                        <li class="text-white uppercase py-2 text-xl font-semibold">Categories</li>
                        <li class="text-sm text-gray-400 py-2">Mobile Printer</li>
                        <li class="text-sm text-gray-400 py-2">Label Printer</li>
                        <li class="text-sm text-gray-400 py-2">Receipt Printer</li>
                        <li class="text-sm text-gray-400 py-2">Thermal Printer</li>
                    </ul>
                </div>
            </div>

            <div class="border-b border-gray-600"></div>

            <!-- Copyright Section -->
            <div class="px-8 flex items-center">
                <p class="text-sm text-gray-400">Copyright © 2022 Rongta Bangladesh</p>
            </div>
        </div>
    </div>
</template>