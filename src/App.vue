<template>
    <div class="overflow-x-hidden h-screen">
        <Navbar></Navbar>
        <router-view></router-view>
    </div>
</template>

<script>
import { defineComponent } from 'vue'
import Navbar from './components/Navbar.vue'

export default defineComponent({
    components: {
        Navbar
    },
    data: () => ({
        showMenu: false,
        showProfileMenu: false,
        links: [
            { text: 'Home', to: '/' },
            { text: 'About', to: '/about' },
        ],
    }),
})
</script>
