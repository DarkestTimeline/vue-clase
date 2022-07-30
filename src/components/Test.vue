<template lang="en">
    <div>
        <h1>Bienvenido a Sistemas Expertos</h1>
        <h3>Operaciones Artimeticas</h3>
        <p>{{Numero}}<sup>2</sup> = {{getCuadrado()}}</p>
        <p>{{Numero}}<sup>3</sup> = {{getCubo()}}</p>
        <p>{{Numero}} = {{getPar()}}</p>
        <!-- Crear botones -->
        <button @click="getDecrementar()">Decrementar</button>
        <button v-on:click="getIncrementar()">Incrementar</button>
        
        <br><br><br><br>
        
        <!-- Ejercicio Clase-->
        <h2>Ejercicio Clase - Esfera</h2>
        <form>
            <label>Ingrese el radio de la esfera: </label>
            <input type="number" id="radioInput" min="1" value="1">
        </form>
        <br>
        <button @click="getRadio">Calcular</button>
        <br>
        <p>El area de la esfera es = {{getAreaEsfera()}}</p>
        <p>El volumen de la esfera es = {{getVolumenEsfera()}}</p>
        <p>El radio es un numero primo? = {{isPrime(this.Radio)}}</p>
        
    </div>
</template>
<script>
export default {
    data() {
        return {
            Numero: 2,
            Radio: 1
        }
        
    },
    methods: {
            // Metodo cuadrado de un numero
            getCuadrado(){
                return this.Numero * this.Numero
            }, 
            getCubo(){
                return this.Numero * this.Numero * this.Numero
            },
            getPar(){
                // Usar un if/else para ver si el numero es par o impara
                if(this.Numero % 2 == 0){
                    return "El numero es par"
                } else {
                    return "El numero es impar"
                }
            },
            getIncrementar(){
                this.Numero++
            },
            getDecrementar(){
                this.Numero--
            },
            getRadio(){
                return parseInt(this.Radio = document.getElementById("radioInput").value)
            },
            getAreaEsfera(){
                return 4 * Math.PI * this.Radio * this.Radio
            },
            getVolumenEsfera(){
                return (4/3) * Math.PI * this.Radio * this.Radio * this.Radio
            },
            isPrime(num) {
                if (num <= 1) return false;
                if (num=== 2) return true;
                let num2 = Math.sqrt(num); //num2 es la raiz cuadrada de num
                for (let i= 2; i <= num2; i++) { //el for recorre num2
                    if (num2 % i === 0) {
                        return false;
                    }
                }
                return true;
                }
        }
}
</script>
<style>
    button{
        background-color: #223c6d;
        border: 3px #edb115 solid;
        border-radius: 8px;
        color: whitesmoke;
        margin: 0px 10px;
        padding: 15px;
        font-size: large;
        cursor: pointer;
    }
    button:hover{
        transition: 0.5s ease-in;
        padding: 20px;
        background-color: #121f39;
    }

    
</style>