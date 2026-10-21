<script>
export default {
    emits: ['closeModal', 'send-to'],
    data() {
        return {
            fullname: '',
            age: null,
            address: '',
            date: '',
            petType: '',
            color:'',
            dogAge:'',
            breed:'',
            petSickness:''

        }
    },
    methods: {
        closeModal(mod) {
            this.$emit('closeModal', mod);
        },
        submitTheForm() {
            this.$emit('send-to', {
                name: this.fullname,
                myAge: this.age,
                myAddress: this.address,
                myDate: this.date,
                myPetType: this.petType,
                myColor: this.color,
                mydogAge: this.dogAge,
                myBreed: this.breed,
                mypetSickness:this.petSickness

            });
            this.closeModal()
        }
    }
}
</script>

<template>
    <div>
        <div class="fixed inset-0 z-50 flex items-center justify-center bg-black/50">
            <div class="bg-white rounded-2xl shadow-xl w-full max-w-3xl p-8">
                <div class="flex justify-between items-center mb-6">
                    <h2 class="text-2xl font-bold">Owner</h2>

                    <button type="button" class="text-2xl font-bold hover:text-red-500">

                    </button>
                </div>

                <div class="flex flex-col gap-5">
                    <div>
                        <label class="gray mb-2 font-medium"></label>

                        <input v-model="fullname" type="text" class="w-50 border rounded-lg px-4 py-3"
                            placeholder="fullname:" />
                        <input v-model="age" type="number" class="w-30 border rounded-lg px-4 py-3"
                            placeholder="Age:" />

                    </div>

                    <div class="flex-1">
                        <label class="block mb-2 font-medium"> </label>
                        <input v-model="address" type="text" class="w-50 border rounded-lg px-4 py-3"
                            placeholder="Address:">
                    </div>
                    <div class="flex-1">
                        <label class="block mb-2 font-medium"> </label>
                        <input v-model="date" type="text" class="w-50  border rounded-lg px-4 py-3" placeholder="Date:">
                    </div>
                </div>

                <div class="flex gap-5">
                    <div class="flex-1">
                        <label class="block mb-2 font-medium"> </label>

                        <input v-model="petSickness" class="w-50 h-50 border rounded-lg px-4 py-3" placeholder="Pet's sickness:">
                    </div>

                    <div class="flex-1">
                        <label class="block mb-2 font-medium"> Pet's </label>

                        <input v-model="petType" class="w-50 border rounded-lg px-4 py-3" placeholder="Pet's type:">
                        <input v-model="color" class="w-50 border rounded-lg px-4 py-3" placeholder="Color:">
                        
                    </div>
                    <div class="flex-1">

                        <input v-model="dogAge" class="w-30 border rounded-lg px-4 py-3" placeholder="Age:">
                        <input v-model="breed" class="w-50 border rounded-lg px-4 py-3" placeholder="Breed:" />
                    </div>
                </div>

                <div class="flex justify-end gap-3 pt-3">
                    <button @click="submitTheForm" class="px-5 py-2 border bg-blue-700  rounded-lg hover:bg-blue-800">
                        Book Now
                    </button>

                    <button @click="closeModal(false)"
                        class="cursor-pointer px-5 py-2 text-red-700 rounded-lg hover:bg-red-200">
                        Cancel
                    </button>
                </div>
            </div>
        </div>
    </div>
</template>