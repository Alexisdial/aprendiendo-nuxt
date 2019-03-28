<template>
<div>
    <!-- <navbar/>  este navbar viene de abajo, lo que se importó -->
    <h1>Hola {{ msg }}</h1> <!-- con las llaves se indica que ahi va condigo javascript. Solo puede haber un elemento padre -->
    <input type="text" v-model="msg"> <!-- Lo enlazado de conecta -->
    <button @click="guardar" class="btn btn-primary">Guardar</button>
    <b-button variant="primary">Guardar</b-button>
    <table>
        <tr>
            <th>Nombre</th>
        </tr>
        <tr v-for="(mun,index) in municipios" :key="index"><!-- seria como mun dentro de municipios, index son las posiciones del for -->
            <td>{{ mun }} </td>
            </tr>  
    </table>
</div>
</template>

<script>
//import navbar from '../Components/navbar'
//import contacto from './contacto'

export default{
   // components: {navbar},

    data(){
        return{
            msg: "Alexis López",
            municipios: ['Mocoa', 'Villagarzon', 'Pto Asis']

        };
    },
    methods: {
        guardar(){
           // alert("guardando...")
            this.municipios.push(this.msg)  /* this hace referencia a la instancia */
            this.msg = ''
        }
    }
}
</script>

<style>

</style>
