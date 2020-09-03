<template>
    <div class="container">
        <h1 class="my-4 text-center">App meteo with Vue.js</h1>

        <div class="form-group mb-5">
            <label for="position">Entrer le nom de la ville</label>
            <input 
                type="text" 
                class="form-control w-75 m-auto"
                id="position"
                v-model="requete"
                v-on:keypress.enter="goMeteo"
            >
        </div>
        <div v-if="temps" class="w-75 m-auto">
            <h3 class="text-center mb-3">Position: {{ temps.name}}</h3>
            <div  class="card text-center p-5">
                <p class="texte-affichage">
                    Temperature: {{temps.main.temp.toFixed()}} degrès
                </p>
                <p class="texte-affichage">
                    Temps: {{temps.weather[0].description}}
                </p>
            </div>
        </div>
    </div>
</template>

<script>
import axios from 'axios'

export default {
    name: 'Meteo',
    data(){
        return{
            requete: '',
            temps: undefined,
            api_code: '0f24f9ceae74774fd8c3f6ec9730fbe6',
            url_appel: 'https://api.openweathermap.org/data/2.5/weather?'
        }
    },

    methods: {
        goMeteo: function(){
            axios
            .get(`${this.url_appel}q=${this.requete}&units=metric&APPID=${this.api_code}&lang=fr`)
            .then(response => {
                this.temps = response.data
                console.log(response)
                this.requete = ""
            })
        }
    }
}
</script>

<style scoped>
.texte-affichage{
    font-size: 25px;
    font-weight: 600;
}
</style>