<template>
    <div class="hidden lg:block w-full h-40 mx-0">
        <div class="h-full px-32 pt-5 bg-gradient-to-r from-red-500 to-red-500 overflow-y-visible">
            <div class="block">
                <div class="flex flex-wrap items-center justify-between w-full">
                    <div class="flex justify-start space-x-5">
                        <div>
                            <a class="text-white" href="#">Seller centre</a>
                        </div>
                        <div class="text-white">|</div>
                        <div class="text-white">
                            <a class="text-white" href="#">Download</a>
                        </div>
                        <div class="text-white">|</div>
                        <div class="text-white flex">
                            Ikuti kami di
                            <svg
                                xmlns="http://www.w3.org/2000/svg"
                                class="h-5 w-5 ml-1"
                                viewBox="0 0 20 20"
                                fill="currentColor"
                            >
                                <path
                                    fill-rule="evenodd"
                                    d="M10.496 2.132a1 1 0 00-.992 0l-7 4A1 1 0 003 8v7a1 1 0 100 2h14a1 1 0 100-2V8a1 1 0 00.496-1.868l-7-4zM6 9a1 1 0 00-1 1v3a1 1 0 102 0v-3a1 1 0 00-1-1zm3 1a1 1 0 012 0v3a1 1 0 11-2 0v-3zm5-1a1 1 0 00-1 1v3a1 1 0 102 0v-3a1 1 0 00-1-1z"
                                    clip-rule="evenodd"
                                />
                            </svg>
                        </div>
                    </div>
                    <div class="flex space-x-5 justify-end">
                        <div>
                            <a href class="text-white">
                                <svg
                                    xmlns="http://www.w3.org/2000/svg"
                                    class="h-5 w-5 inline"
                                    viewBox="0 0 20 20"
                                    fill="currentColor"
                                >
                                    <path
                                        d="M10 2a6 6 0 00-6 6v3.586l-.707.707A1 1 0 004 14h12a1 1 0 00.707-1.707L16 11.586V8a6 6 0 00-6-6zM10 18a3 3 0 01-3-3h6a3 3 0 01-3 3z"
                                    />
                                </svg>
                                Notifikasi
                            </a>
                        </div>
                        <div>
                            <a href class="text-white">
                                <svg
                                    xmlns="http://www.w3.org/2000/svg"
                                    class="h-6 w-6 inline"
                                    fill="none"
                                    viewBox="0 0 24 24"
                                    stroke="currentColor"
                                >
                                    <path
                                        stroke-linecap="round"
                                        stroke-linejoin="round"
                                        stroke-width="2"
                                        d="M8.228 9c.549-1.165 2.03-2 3.772-2 2.21 0 4 1.343 4 3 0 1.4-1.278 2.575-3.006 2.907-.542.104-.994.54-.994 1.093m0 3h.01M21 12a9 9 0 11-18 0 9 9 0 0118 0z"
                                    />
                                </svg>
                                Bantuan
                            </a>
                        </div>
                        <div>
                            <a class="text-white" href>Ricky Andhika</a>
                        </div>
                    </div>
                </div>
            </div>
            <div class="block mt-5">
                <div class="flex justify-between items-center">
                    <div>
                        <a href="#" class="text-black flex items-center space-x-5">
                            <img class="h-16 w-16" src="/img/smile.svg" />
                            <span class="text-4xl text-white font-bold">Shopy</span>
                        </a>
                    </div>
                    <div class="w-1/2 flex relative">
                        <input
                            type="text"
                            class="outline-none px-2 h-12 w-10/12 border-0 rounded-l focus:border focus:border-white"
                            @focus="toggleIsSearchTypeHeadOpened"
                            @blur="toggleIsSearchTypeHeadOpened"
                        />
                        <div
                            class="w-1/6 p-2 border-0 rounded-l-none h-12 bg-white rounded font-semibold box-border"
                        >
                            <button class="p-1 bg-red-500 w-full text-center text-white">
                                <svg
                                    xmlns="http://www.w3.org/2000/svg"
                                    class="h-6 w-6 mx-auto"
                                    fill="none"
                                    viewBox="0 0 24 24"
                                    stroke="currentColor"
                                >
                                    <path
                                        stroke-linecap="round"
                                        stroke-linejoin="round"
                                        stroke-width="2"
                                        d="M21 21l-6-6m2-5a7 7 0 11-14 0 7 7 0 0114 0z"
                                    />
                                </svg>
                            </button>
                        </div>
                        <div v-if="isSearchTypeHeadOpened" class="w-full h-100 absolute bg-white top-14 shadow-lg p-2 rounded overflow-y-visible z-50">
                            <a href="#" class="block p-2 hover:bg-gray-200">
                                smdksdmksmkdsd
                            </a>
                            <a href="#" class="block p-2 hover:bg-gray-200">
                                smdksdmksmkdsd
                            </a>
                            <a href="#" class="block p-2 hover:bg-gray-200">
                                smdksdmksmkdsd
                            </a>
                        </div>
                    </div>
                    <div class="relative">
                        <a @click="toggleIsCarOpened" href="#" class="text-white">
                            <svg
                                xmlns="http://www.w3.org/2000/svg"
                                class="h-8 w-8"
                                fill="none"
                                viewBox="0 0 24 24"
                                stroke="currentColor"
                            >
                                <path
                                    stroke-linecap="round"
                                    stroke-linejoin="round"
                                    stroke-width="2"
                                    d="M3 3h2l.4 2M7 13h10l4-8H5.4M7 13L5.4 5M7 13l-2.293 2.293c-.63.63-.184 1.707.707 1.707H17m0 0a2 2 0 100 4 2 2 0 000-4zm-8 2a2 2 0 11-4 0 2 2 0 014 0z"
                                />
                            </svg>
                        </a>
                        <span class="font-xs absolute -top-3 -right-1 p-1 bg-white rounded-lg">1</span>
                        <div
                            v-if="isCartOpened"
                            class="absolute right-0 mt-2 pt-4 w-96 bg-white rounded-md shadow-xl z-20"
                        >
                            <div class="block px-3">
                                <span class="opacity-50">Baru ditambahkan</span>
                            </div>
                            <div class="block mt-2">
                                <div class="flex justify-between p-2 items-start space-x-1 hover:bg-gray-200 px-3">
                                    <div>
                                        <img class="h10 w-10" src="/img/hoodie.jpeg" alt />
                                    </div>
                                    <div>
                                        <span class="font-semibold">Roughneck H012 Black</span>
                                    </div>
                                    <div>
                                        <span class="text-sm">Rp. 150.000</span>
                                    </div>
                                </div>
                                <div class="flex justify-between p-2 items-start space-x-1 hover:bg-gray-200 px-3">
                                    <div>
                                        <img class="h10 w-10" src="/img/hoodie.jpeg" alt />
                                    </div>
                                    <div>
                                        <span class="font-semibold">Roughneck H012 Black</span>
                                    </div>
                                    <div>
                                        <span class="text-sm">Rp. 150.000</span>
                                    </div>
                                </div>
                            </div>
                            <div class="block text-right p-5">
                                <button
                                    class="h-10 rounded bg-red-500 text-white p-2 font-semibold"
                                >Ke keranjang belanja</button>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
    <div class="block lg:hidden w-full h-20 mx-0 bg-gray-100">
        <div class="h-full max-w-xl mx-auto pt-5 bg-gradient-to-r from-red-500 to-red-500">
            <div class="flex h-14 items-center justify-between px-5 space-x-0">
                <div class="w-9/12 ml-3 h-9 inline-flex">
                    <button class="h-full bg-white rounded-l border-none p-2">
                        <svg
                            xmlns="http://www.w3.org/2000/svg"
                            class="h-4 w-4"
                            fill="none"
                            viewBox="0 0 24 24"
                            stroke="currentColor"
                        >
                            <path
                                stroke-linecap="round"
                                stroke-linejoin="round"
                                stroke-width="2"
                                d="M21 21l-6-6m2-5a7 7 0 11-14 0 7 7 0 0114 0z"
                            />
                        </svg>
                    </button>
                    <input
                        type="text"
                        class="outline-none px-2 h-full w-full rounded-r border-none hover:border"
                    />
                </div>
                <div class="relative">
                    <a href="#" class="text-white">
                        <svg
                            xmlns="http://www.w3.org/2000/svg"
                            class="h-7 w-7"
                            fill="none"
                            viewBox="0 0 24 24"
                            stroke="currentColor"
                        >
                            <path
                                stroke-linecap="round"
                                stroke-linejoin="round"
                                stroke-width="2"
                                d="M3 3h2l.4 2M7 13h10l4-8H5.4M7 13L5.4 5M7 13l-2.293 2.293c-.63.63-.184 1.707.707 1.707H17m0 0a2 2 0 100 4 2 2 0 000-4zm-8 2a2 2 0 11-4 0 2 2 0 014 0z"
                            />
                        </svg>
                    </a>
                    <span
                        class="bg-white p-1 h-5 w-5 text-xs text-center rounded-xl absolute -top-2 -right-1 font-medium"
                    >1</span>
                </div>
                <div>
                    <a href="#" class="text-white">
                        <svg
                            xmlns="http://www.w3.org/2000/svg"
                            class="h-7 w-7"
                            fill="none"
                            viewBox="0 0 24 24"
                            stroke="currentColor"
                        >
                            <path
                                stroke-linecap="round"
                                stroke-linejoin="round"
                                stroke-width="2"
                                d="M16 7a4 4 0 11-8 0 4 4 0 018 0zM12 14a7 7 0 00-7 7h14a7 7 0 00-7-7z"
                            />
                        </svg>
                    </a>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
import { defineComponent, ref } from 'vue';

export default defineComponent({
    setup() {
        let isCartOpened = ref(false);
        let isSearchTypeHeadOpened = ref(false);

        const toggleIsCarOpened = () => {
            isCartOpened.value = !isCartOpened.value;
        }

        const toggleIsSearchTypeHeadOpened = () => {
            isSearchTypeHeadOpened.value = !isSearchTypeHeadOpened.value;
        }

        return {
            isCartOpened,
            isSearchTypeHeadOpened,

            toggleIsCarOpened,
            toggleIsSearchTypeHeadOpened
        };
    },
})
</script>
