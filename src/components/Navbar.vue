<script>
export default {
    data() {
        return {

        }
    },
    methods: {
        navi(page) {
            this.$emit('goTo', page);
        },
        openModal(modal) {
            this.$emit('openModal', modal);
        }
    }
}

</script>

<template>
    <header class="bg-white">
        <nav class="container mx-auto px-4 py-4 flex justify-between items-center">
            <a href="#" class="text-2xl font-bold transition-colors duration-300">
                <img src="../assets/images/vet-logo.png" alt="" class="w-30 h-20">
            </a>
            <div class="hidden md:flex space-x-6">
                <p @click="navi('Home')" class="cursor-pointer text-[#134288] font-semibold duration-300">Home</p>
                <p @click="navi('Appointments')" class="cursor-pointer text-[#134288] font-semibold duration-300">
                    Appointments</p>
            </div>
            <div class="hidden md:flex items-center space-x-4">
                <p @click="openModal(true)"
                    class="bg-[#F25457] text-white px-4 py-2 rounded-lg hover:bg-blue-900 transition-colors duration-300 text-[20px] font-bold">
                    BOOK
                    NOW</p>
            </div>
            <button id="mobileMenuButton"
                class="md:hidden text-gray-700 dark:text-gray-200 hover:text-indigo-800 dark:hover:text-white focus:outline-none transition-colors duration-300">
                <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24"
                    stroke="currentColor">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16" />
                </svg>
            </button>
        </nav>
        <!-- <div id="mobileMenu"
            class="mobile-menu md:hidden bg-white dark:bg-gray-800 shadow-lg absolute w-full left-0 transform -translate-y-full opacity-0">
            <div class="container mx-auto px-4 py-4 space-y-4">
                <p class=" text-gray-700 text-[#134288] font-semibold duration-300">Home</p>
                <p class=" text-gray-700 text-[#134288] font-semibold duration-300">Appointments</p>
                <div class="hidden md:flex items-center space-x-4">
                    <a href="#"
                        class="bg-[#F25457] text-white px-4 py-2 rounded-lg hover:bg-blue-900 transition-colors duration-300 text-[20px] font-bold">BOOK
                        NOW</a>
                </div>
            </div>
        </div> -->
    </header>
</template>