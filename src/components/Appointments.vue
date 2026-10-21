<script>
    export default{
        props:['sendForm'],
    }
</script>

<template>
    <div class="mx-[100px] mt-10">
        <div v-for="details in sendForm" class="my-2 w-full shadow-xl rounded-[15px] bg-[#F7F7F7] h-[387px] grid grid-cols-2 py-[52px] px-[46px]">
            <div>
                <p class="text-[#134288] text-[24px] text-center border-b-2 border-[#134288]/50 mr-5">Owner</p>
                <div class="flex mb-2 gap-2">
                    <p class="text-[#134288] text-[24px]">Name:</p>
                    <p class="text-[#134288]/80 font-semibold text-[24px]">{{ details.name }}</p>
                </div>
                <div class="flex mb-2 gap-2">
                    <p class="text-[#134288] text-[24px]">Age:</p>
                    <p class="text-[#134288]/80 font-semibold text-[24px]">{{ details.myAge }}</p>
                </div>
                <div class="flex">
                    <p class="text-[#134288] text-[24px]">Address:</p>
                    <p class="text-[#134288]/80 font-semibold text-[24px]">{{ details.myAddress }}</p>
                </div>
                <div class="">
                    <p class="text-[#134288] text-[24px] text-center border-b-2 border-[#134288]/50 mr-5">Pet</p>
                    <div class="grid grid-cols-2 m-2">
                        <div class="flex items-center gap-2">
                            <p class="text-[#134288] text-[24px]">Pet type:</p>
                            <p class="text-[#134288]/80 font-semibold text-[24px]">{{ details.myPetType }} </p>
                        </div>
                        <div class="flex items-center gap-2">
                            <p class="text-[#134288] text-[24px]">Color:</p>
                            <p class="text-[#134288]/80 font-semibold text-[24px]"> {{ details.myColor }}</p>
                            
                        </div>
                    </div>
                    <div class="grid grid-cols-2 m-2 gap-2">
                        <div class="flex items-center gap-2">
                            <p class="text-[#134288] text-[24px]">Age:</p>
                            <p class="text-[#134288]/80 font-semibold text-[24px]"> {{ details.mydogAge }}</p>
                            
                        </div>
                        <div class="flex items-center gap-2">
                            <p class="text-[#134288] text-[24px]">Breed:</p>
                            <p class="text-[#134288]/80 font-semibold text-[24px]"> {{ details.myBreed }}</p>
                            
                        </div>
                    </div>
                </div>
            </div>
            <div>
            <div>
                <div class="flex justify-end px-5">
                    <select class="text-[#134288] text-[20px] cursor-pointer">
                        <option value="" >Actions</option>
                    </select>
                </div>
                <div class="flex gap-2">
                    <p class="text-[#134288] text-[24px]">Date:</p>
                    <p class="text-[#134288]/80 font-semibold text-[24px]">{{ details.myDate }}</p>
                </div>
                <div>
                    <div placeholder="Pet's sickness" class="w-full max-h-60 h-60 bg-[#E9E9E9] p-5 rounded-[15px]"> {{ details.mypetSickness }}</div>
                </div>
            </div>
            </div>
        </div>

    </div>
</template>