<template>
    <div class="block lg:hidden  bg-gray-100 h-full">
        <div class="relative h-50 w-full mx-auto max-w-xl overflow-x-hidden">
            <img @touchstart="onTouchStart" @touchend="onTouchEnd" :class="{ 'animate-slide-left': animateToLeft, 'animate-slide-right' : animateToRight }" class="h-full w-full" :src="currentImageUrl" />
            <div class="flex absolute px-5 space-x-1 items-center" style="left: 5%; top: 80%;">
                <div v-for="n in (numberOfImages)" :key="n" class="font-bold text-white">
                    <span v-if="n === currentImageIndex + 1">
                        -
                    </span>
                    <span class="text-xs" v-else>
                        o
                    </span>
                </div>
            </div>
        </div>
        <div class="flex w-full mx-auto max-w-xl mt-5 space-x-5 items-start px-5 bg-white rounded">
            <div class="w-28 p-3  text-center align-middle">
               <svg xmlns="http://www.w3.org/2000/svg" class="h-8 w-8 mx-auto" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 12l2-2m0 0l7-7 7 7M5 10v10a1 1 0 001 1h3m10-11l2 2m-2-2v10a1 1 0 01-1 1h-3m-6 0a1 1 0 001-1v-4a1 1 0 011-1h2a1 1 0 011 1v4a1 1 0 001 1m-6 0h6" />
                </svg>
                <span class="text-xs">Shopee dari rumah</span>
            </div>
            <div class="w-28 p-3 text-center">
                <svg xmlns="http://www.w3.org/2000/svg" class="h-8 w-8 mx-auto" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 18h.01M8 21h8a2 2 0 002-2V5a2 2 0 00-2-2H8a2 2 0 00-2 2v14a2 2 0 002 2z" />
                </svg>
                <span class="text-xs">Pulsa</span>
            </div>
            <div class="w-28 p-3  text-center align-middle">
                <svg xmlns="http://www.w3.org/2000/svg" class="h-8 w-8 mx-auto" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 3h2l.4 2M7 13h10l4-8H5.4M7 13L5.4 5M7 13l-2.293 2.293c-.63.63-.184 1.707.707 1.707H17m0 0a2 2 0 100 4 2 2 0 000-4zm-8 2a2 2 0 11-4 0 2 2 0 014 0z" />
                </svg>  
                <span class="text-xs">Belanja</span>
            </div>
            <div class="w-28 p-3  text-center align-middle">
                <svg xmlns="http://www.w3.org/2000/svg" class="h-8 w-8 mx-auto" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M16 11V7a4 4 0 00-8 0v4M5 9h14l1 12H4L5 9z" />
                </svg>
                <span class="text-xs">Mall</span>
            </div>
        </div>
    </div>

    <div class="hidden lg:block h-full pt-7 bg-gray-100" style="background: url('https://cf.shopee.co.id/file/44d1be7cc5fe00671ebd875ed45407d1') center top / 100% no-repeat;">
        <div class="flex mx-auto w-4/6 h-58 space-x-1">
            <div class="h-full w-8/12">
                <img src="/img/banner.jpeg" class="w-full h-full">
            </div>
            <div class="flex flex-col h-full w-4/12 space-y-1 justify-between align-middle">
                <div class="h-1/2">
                    <img src="/img/mini-banner.png" class="h-full w-full" alt="">
                </div>
                <div class="h-1/2">
                    <img src="/img/mini-banner.png" class="h-full w-full" alt="">
                </div>
            </div>
        </div>

        <div class="bg-white mt-3 flex mx-auto w-4/6">
            <div class="w-28 p-3  text-center align-middle">
                <svg xmlns="http://www.w3.org/2000/svg" class="h-8 w-8 mx-auto" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 12l2-2m0 0l7-7 7 7M5 10v10a1 1 0 001 1h3m10-11l2 2m-2-2v10a1 1 0 01-1 1h-3m-6 0a1 1 0 001-1v-4a1 1 0 011-1h2a1 1 0 011 1v4a1 1 0 001 1m-6 0h6" />
                </svg>
                <span class="text-xs">Shopee dari rumah</span>
            </div>
            <div class="w-28 p-3 text-center">
                <svg xmlns="http://www.w3.org/2000/svg" class="h-8 w-8 mx-auto" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 18h.01M8 21h8a2 2 0 002-2V5a2 2 0 00-2-2H8a2 2 0 00-2 2v14a2 2 0 002 2z" />
                </svg>
                <span class="text-xs">Pulsa</span>
            </div>
            <div class="w-28 p-3  text-center align-middle">
                <svg xmlns="http://www.w3.org/2000/svg" class="h-8 w-8 mx-auto" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 3h2l.4 2M7 13h10l4-8H5.4M7 13L5.4 5M7 13l-2.293 2.293c-.63.63-.184 1.707.707 1.707H17m0 0a2 2 0 100 4 2 2 0 000-4zm-8 2a2 2 0 11-4 0 2 2 0 014 0z" />
                </svg>  
                <span class="text-xs">Belanja</span>
            </div>
            <div class="w-28 p-3  text-center align-middle">
                <svg xmlns="http://www.w3.org/2000/svg" class="h-8 w-8 mx-auto" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M16 11V7a4 4 0 00-8 0v4M5 9h14l1 12H4L5 9z" />
                </svg>
                <span class="text-xs">Mall</span>
            </div>
            <div class="w-28 p-3  text-center align-middle">
                <svg xmlns="http://www.w3.org/2000/svg" class="h-8 w-8 mx-auto" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 14l-7 7m0 0l-7-7m7 7V3" />
                </svg>
                <span class="text-xs">Murah lebay</span>
            </div>
            <div class="w-28 p-3  text-center align-middle">
                <svg xmlns="http://www.w3.org/2000/svg" class="h-8 w-8 mx-auto" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17 9V7a2 2 0 00-2-2H5a2 2 0 00-2 2v6a2 2 0 002 2h2m2 4h10a2 2 0 002-2v-6a2 2 0 00-2-2H9a2 2 0 00-2 2v6a2 2 0 002 2zm7-5a2 2 0 11-4 0 2 2 0 014 0z" />
                </svg>
                <span class="text-xs">COD</span>
            </div>
            <div class="w-28 p-3 text-center align-middle relative">
                <a href="#" class="hover:text-red-500">
                    <svg xmlns="http://www.w3.org/2000/svg" class="h-8 w-8 mx-auto" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M16 7a4 4 0 11-8 0 4 4 0 018 0zM12 14a7 7 0 00-7 7h14a7 7 0 00-7-7z" />
                    </svg>
                    <span class="text-xs">Fashion</span>
                </a>
            </div>
            <div class="w-28 p-3 text-center align-middle relative">
                <a href="#" class="hover:text-red-500">
                    <svg fill="none" stroke="currentColor" stroke-width="10" class="h-8 w-8 mx-auto" version="1.1" viewBox="0 0 256 256" xml:space="preserve" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink">
                        <g>
                            <path d="M137.5,110.5c-3.5-2.1-7.1-4.2-10.7-6.2l-12.3-7.1c-7.6-4.4-16.2-9.4-24.6-14c-3.8-2.1-7.4-2.4-10.1-0.9   c-2.7,1.5-4.2,4.7-4.4,8.9c-0.2,6.5-0.2,13.2-0.1,20c0,2.9,0,5.9,0,8.8l-0.1,9c0,6.3-0.1,12.9,0.1,19.4c0.1,4.5,1.6,7.8,4.2,9.4   c1.2,0.7,2.5,1.1,4,1.1c2,0,4.1-0.6,6.4-1.7c0.5-0.2,1-0.5,1.4-0.8l8.8-5.1c12.6-7.3,25.2-14.5,37.8-21.9c1.6-0.9,2.9-1.9,4-3   c3.8-3.9,3.8-8.5-0.1-12.4C140.5,112.4,138.8,111.3,137.5,110.5z M133.1,120.6c-12.6,7.3-25.2,14.6-37.7,21.8l-8.8,5.1   c-0.3,0.2-0.6,0.3-0.9,0.5c-0.1,0.1-0.2,0.1-0.3,0.1c0-0.1,0-0.1,0-0.2c-0.1-6.3-0.1-12.8-0.1-19.3l0.1-8.7c0-3,0-5.9-0.1-9.3   c-0.1-6.2-0.1-12.5,0.1-18.7c8.2,4.5,16.7,9.4,24.2,13.8l12.3,7.1c3.5,2,7.1,4,10.5,6.1v0c0.3,0.2,1,0.6,1.6,1   C133.7,120.3,133.4,120.4,133.1,120.6z"/><path d="M210.7,27.2H45.4C23,27.2,4.9,45.4,4.9,67.7v104.6c0,22.3,18.2,40.5,40.5,40.5h19.2v11c0,2.7,2.2,5,5,5c2.7,0,5-2.2,5-5   v-11h107v11c0,2.7,2.2,5,5,5c2.7,0,5-2.2,5-5v-11h19.2c22.3,0,40.5-18.2,40.5-40.5V67.7C251.1,45.4,233,27.2,210.7,27.2z    M241.2,172.3c0,16.8-13.7,30.6-30.6,30.6H45.4c-16.8,0-30.6-13.7-30.6-30.6V67.7c0-16.8,13.7-30.6,30.6-30.6h165.3   c16.8,0,30.6,13.7,30.6,30.6V172.3z"/><path d="M174.8,54.3H45.4c-7.4,0-13.4,6-13.4,13.4v104.6c0,7.4,6,13.4,13.4,13.4h129.4c7.4,0,13.4-6,13.4-13.4V67.7   C188.2,60.3,182.2,54.3,174.8,54.3z M178.2,172.3c0,1.9-1.6,3.5-3.5,3.5H45.4c-1.9,0-3.5-1.6-3.5-3.5V67.7c0-1.9,1.6-3.5,3.5-3.5   h129.4c1.9,0,3.5,1.6,3.5,3.5V172.3z"/><circle cx="214.6" cy="95.4" r="6.3"/><circle cx="214.6" cy="67.3" r="6.3"/>
                        </g>
                    </svg>
                    
                    <span class="text-xs">Fashion</span>
                </a>
            </div>
        </div>

        <div class="bg-white mt-3 mx-auto w-4/6">
            <div class="block p-2">
                <span class="text-red-500">Kategori</span>
            </div>
            <div class="flex">

            </div>
        </div>
    </div>
</template>

<script>
import { defineComponent, ref, onMounted } from 'vue';

export default defineComponent({
    setup() {

        let currentImageIndex = ref(0);

        let touchStartXPosition = 0;
        let touchEndXPosition = 0;

        let animateToLeft = ref(false);
        let animateToRight = ref(false);

        const imagesSliders = [
            {
                url: '/img/bg.png'
            },
            {
                url: '/img/bg2.png'
            }
        ];

        const numberOfImages = imagesSliders.length;
        let currentImageUrl = ref(imagesSliders[currentImageIndex.value].url);

        const slideImageToLeft = () => {
            animateToLeft.value = true;
            setTimeout(() => {
                animateToLeft.value = false;
                currentImageIndex.value = currentImageIndex.value - 1;
                if  (currentImageIndex.value < 0) {
                    currentImageIndex.value = numberOfImages - 1;
                }
                currentImageUrl.value = imagesSliders[currentImageIndex.value].url;
            }, 500);
        }

        const slideImageToRight = () => {
            animateToRight.value = true;
            setTimeout(() => {
                animateToRight.value = false;
                currentImageIndex.value = currentImageIndex.value + 1;
                if (currentImageIndex.value > (numberOfImages - 1)) {
                    currentImageIndex.value = 0;
                }
                currentImageUrl.value = imagesSliders[currentImageIndex.value].url;
            }, 500);
        }
        
        const onTouchStart = (event) => {
            const changedTouches = event.changedTouches;
            if (changedTouches.length) {
                touchStartXPosition = changedTouches[0].clientX;
            }
        }

        const onTouchEnd = (event) => {
            const changedTouches = event.changedTouches;
            if (changedTouches.length) {
                touchEndXPosition = changedTouches[0].clientX;
                if (touchEndXPosition  < touchStartXPosition) {
                    slideImageToLeft();
                } else {
                    slideImageToRight();
                }
            }
        }

        onMounted(function () {
            setInterval(() => {
                slideImageToRight();
            }, 6000);
        });

        return {
            animateToLeft,
            animateToRight,
            currentImageUrl,
            numberOfImages,
            currentImageIndex,

            onTouchStart,
            onTouchEnd
        };
    },
})
</script>

<style>
.animate-slide-left {
    transform: translateX(-100%);
    transition: transform 0.5s;
}

.animate-slide-right {
    transform: translateX(100%);
    transition: transform 0.5s;
}
</style>
