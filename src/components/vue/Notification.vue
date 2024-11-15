<script setup>

import { ref } from "vue";

let qty = ref(0)

function add() {
    qty.value++
    console.log(qty)

}

function menos() {
    if (qty.value == 0) {
        qty.value
}
    else{
        qty.value--
    }
}
</script>

<template>
    <div class="max-w-80 mx-auto p-6 bg-purple-300 rounded">
        <div v-if="qty > 0"
            class="bg-red-500 text-white size-8 rounded-full text-center flex justify-center items-center font-bold ml-3"
            :class="{'bg-blue-700' : qty > 3}"
        >
            {{ qty }}
        </div>
        <div v-else>
            Nadie te visita :( 
        </div>
        <div class="flex gap-2 mt-2">
            <div 
                @click="add" class="bg-blue-400 text-white rounded size-6 flex justify-center items-center hover:cursor-pointer">
                +
            </div>

            <div 
                @click="menos" class="bg-blue-400 text-white rounded size-6 flex justify-center items-center hover:cursor-pointer">
                -
            </div>

        </div>

    </div>
</template>