<script setup>
import { ref } from 'vue';

const nombre = ref('Chase')
const leerNombre = e => {
    nombre.value = e.target.value
}
</script>
<template>
    <div class="md:w-1/2">
        <h2 class="font-black text-3xl text-center">Seguimiento Pacientes</h2>
        <p class="text-lg mt-5 text-center mb-10">
            Añade Pacientes y
            <span class="text-indigo-600 font-bold">Adminístralos</span>
        </p>
        <form 
            class="bg-white shadow-md rounded-lg py-10 px-5 mb-10"
        >
        {{ nombre }}
            <div class="mb-5">
                <label 
                    class="block text-gray-700 uppercase font-bold"
                    for="mascota"
                >
                    Nombre Mascota
                </label>

                <input
                    id="mascota"
                    type="text"
                    placeholder="Nombre de la mascota"
                    class="border-2 w-full p-2 mt-2 placeholder-gray-400 rounded-md"
                    :value="nombre"
                    @input="leerNombre"
                />
            </div>

            <div class="mb-5">
                <label 
                    class="block text-gray-700 uppercase font-bold"
                    for="propietario"
                >
                    Nombre Propietario
                </label>

                <input
                    id="propietario"
                    type="text"
                    placeholder="Nombre del propietario"
                    class="border-2 w-full p-2 mt-2 placeholder-gray-400 rounded-md"
                />
            </div>

            <div class="mb-5">
                <label 
                    class="block text-gray-700 uppercase font-bold"
                    for="email"
                >
                    Email
                </label>

                <input
                    id="email"
                    type="email"
                    placeholder="Email del propietario"
                    class="border-2 w-full p-2 mt-2 placeholder-gray-400 rounded-md"
                />
            </div>

            <div class="mb-5">
                <label 
                    class="block text-gray-700 uppercase font-bold"
                    for="alta"
                >
                    Fecha Alta
                </label>

                <input
                    id="alta"
                    type="date"
                    class="border-2 w-full p-2 mt-2 placeholder-gray-400 rounded-md"
                />
            </div>

            <div class="mb-5">
                <label 
                    class="block text-gray-700 uppercase font-bold"
                    for="sintomas"
                >
                    Síntomas
                </label>

                <textarea
                    id="sintomas"
                    placeholder="Describe los síntomas"
                    class="border-2 w-full p-2 mt-2 placeholder-gray-400 rounded-md h-40"
                />
            </div>

            <input
                type="submit"
                class="bg-indigo-600 w-full p-3 text-white uppercase font-bold hover:bg-indigo-700 cursor-pointer transition-colors"
                value="Registrar paciente"
            />
        </form>
    </div>
</template>
