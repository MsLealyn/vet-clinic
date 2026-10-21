<script>

</script>

<template>
    <footer class=" border-t-2 border-gray-400 mt-auto">

        <!-- QUICK LINKS -->
        <div class="bg-[#E6F0FD] flex w-full justify-evenly pt-10">
            <div class="w-100 h-100grid grid-cols-1">

                <h2 class="text-xl font-bold">
                    Quick Links
                </h2>
                <p @click="navi('Home')" class="cursor-pointer font-semibold duration-300 text-black hover:text-blue-500">Home</p>
                <p @click="navi('Appointments')" class="cursor-pointer font-semibold duration-300 text-black hover:text-blue-500">
                    Appointments</p>
            </div>

            <div class="grid grid-cols-1">


                <h2 class="text-xl font-bold">
                    Contact Us
                </h2>
                <div class="flex">

                    <div class="  flex flex-wrap ">
                        <div class="w-30 px-4 mb-4">
                            <img src="..//assets/images/linkedin.png" alt="">
                        </div>
                    </div>
                    <div class="  flex flex-wrap ">
                        <div class="w-30 px-4 mb-4">
                            <img src="../assets/images/instagram.png" alt="">
                        </div>
                    </div>
                    <div class="flex flex-wrap ">
                        <div class="w-30 px-4 mb-4">
                            <img src="../assets/images/facebook.png" alt="">
                        </div>
                    </div>
                    <div class=" flex flex-wrap ">

                        <div class="w-30 px-4 mb-4">
                            <img src="../assets/images/telegram.png" alt="">
                        </div>
                    </div>

                </div>
            </div>
        </div>


    </footer>
</template>