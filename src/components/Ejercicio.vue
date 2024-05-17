<script setup>
import {ref} from 'vue';

const showT1 = ref(false)
const showT2 = ref(false)
const showT3 = ref(false)
const showT4 = ref(false)

function showInfo (index){
    
    if(index == 1){

        showT1.value = true
        showT2.value = false
        showT3.value = false
        showT4.value = false

    }
     
        if(index == 2){

        showT1.value = false
        showT2.value = true
        showT3.value = false
        showT4.value = false

        }   
        if(index == 3){

        showT1.value = false
        showT2.value = false
        showT3.value = true
        showT4.value = false

        }   
        if(index == 4){

        showT1.value = false
        showT2.value = false
        showT3.value = false
        showT4.value = true

        }   



    
}

</script>

<template>

<div class="bg-blue-500 p-1 max-w-60 mx-auto mt-12  ">

    <div>
       <h1  @click="showInfo(1)" class=" select-none cursor-pointer bg-blue-300 text-white px-1 justify-between flex">
        
        tema1
        <span class="">{{ showT1 ? '-': '+' }}</span>
    </h1>
       
       <div v-show="showT1" class="bg-slate-200 mt-1 p-1">texto del tema </div>
       <h1  @click="showInfo(2)" class=" select-none cursor-pointer bg-blue-300 text-white px-1 justify-between flex">
        
        tema2
        <span class="">{{ showT2 ? '-': '+' }}</span>
    </h1>
       
       <div v-show="showT2" class="bg-slate-200 mt-1 p-1">texto del tema </div>
       <h1  @click="showInfo(3)" class=" select-none cursor-pointer bg-blue-300 text-white px-1 justify-between flex">
        
        tema3
        <span class="">{{ showT3 ? '-': '+' }}</span>
    </h1>
       
       <div v-show="showT3" class="bg-slate-200 mt-1 p-1">texto del tema </div>
       <h1  @click="showInfo(4)" class=" select-none cursor-pointer bg-blue-300 text-white px-1 justify-between flex">
        
        tema4
        <span class="">{{ showT4 ? '-': '+' }}</span>
    </h1>
       
       <div v-show="showT4" class="bg-slate-200 mt-1 p-1">texto del tema </div>
    </div>

</div>

</template>