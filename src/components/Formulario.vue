<template>
    <div class="md:w-1/2">
        <h2 class="font-black text-3xl text-center">Seguimiento Pacientes</h2>

        <p class="text-lg mt-5 text-center mb-10">
            Añade pacientes y 
            <span class="text-indigo-600 font-bold">Administralos</span>
        </p>

        <form 
            class="bg-white shadow-md rounded-lg py-10 px-5 mb-10"
            @submit.prevent="validar"
        >

            <!-- Begin Input -->
            <div class="mb-5">
                <label 
                    for="mascota"
                    class="block text-gray-700 uppercase font-bold"
                >
                    Nombre Mascota
                </label>
                <input 
                    type="text"
                    id="mascota"
                    placeholder="Nombre de la mascota"
                    class="border-2 w-full p-2 mt-2 placeholder-gray-400 rounded-md"
                    v-model="paciente.nombre"
                />
            </div>
            <!-- End Input -->


            <!-- Begin Input -->
            <div class="mb-5">
                <label 
                    for="propietario"
                    class="block text-gray-700 uppercase font-bold"
                >
                    Nombre Propietario
                </label>
                <input 
                    type="text"
                    id="propietario"
                    placeholder="Nombre del propietario"
                    class="border-2 w-full p-2 mt-2 placeholder-gray-400 rounded-md"
                    v-model="paciente.propietario"
                />

            </div>
            <!-- End Input -->



            <!-- Begin Input -->
            <div class="mb-5">
                <label 
                    for="email"
                    class="block text-gray-700 uppercase font-bold"
                >
                    Email
                </label>
                <input 
                    type="email"
                    id="email"
                    placeholder="Email del propietario"
                    class="border-2 w-full p-2 mt-2 placeholder-gray-400 rounded-md"
                    v-model="paciente.email"
                />
            </div>
            <!-- End Input -->


            <!-- Begin Input -->
            <div class="mb-5">
                <label 
                    for="alta"
                    class="block text-gray-700 uppercase font-bold"
                >
                    Fecha de Alta
                </label>
                <input 
                    type="date"
                    id="alta"
                    class="border-2 w-full p-2 mt-2 placeholder-gray-400 rounded-md"
                    v-model="paciente.alta"
                />
            </div>
            <!-- End Input -->


             <!-- Begin Input -->
             <div class="mb-5">
                <label 
                    for="sintomas"
                    class="block text-gray-700 uppercase font-bold"
                >
                    Síntomas
                </label>
                <textarea
                    id="alta"
                    placeholder="Describe los síntomas"
                    class="border-2 w-full p-2 mt-2 placeholder-gray-400 rounded-md h-40"
                    v-model="paciente.sintomas"
                ></textarea>
            </div>
            <!-- End Input -->

            <input 
                type="submit"
                class="bg-indigo-600 rounded-lg w-full p-3 text-white uppercase font-bold hover:bg-indigo-700 cursor-pointer transition-colors"
                value="Registrar Paciente"
            />


        </form>

    </div>
</template>



<script setup>

import { reactive } from 'vue';



const paciente = reactive({
    nombre: '',
    propietario: '',
    email: '',
    alta: '',
    sintomas: '',
})


const validar = () => {
    console.log('Validando...');
}




</script>

