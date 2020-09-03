<template>
    <div class="container">
        <h1 class="my-4 text-center">App meteo with Vue.js</h1>

        <div class="form-group mb-5">
            <label for="position">Entrer le nom de la ville</label>
            <input 
                type="text" 
                class="form-control"
                id="position"
                v-model="request"
                v-on:keypress="goMeteo"
            >
        </div>
        <div class="w-75 m-auto">
            <h3 class="text-center mb-3">Position: Paris</h3>
            <div class="card text-center p-5">
                <p class="texte-affichage">
                    Temperature: 26 deg
                </p>
                <p class="texte-affichage">
                    Temps: Nuageux
                </p>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'Meteo',
    data(){
        return{

        }
    }
}
</script>

<style scoped>

</style>