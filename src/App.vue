<script setup>
import { ref } from 'vue'

// VARIABLES
const msg = ref('Salut, bienvenue sur ma page Vue.JS')
const count = ref(0)

/*msg.value = "Bonjour"*/ /*--permet de changer le ref de mon message--*/



//FUNCTION

const incrementCount = () => {
  count.value++
}



const resetCount = () => {
  count.value = 0
}



const changeMsg = () => {
  msg.value = "Bravo it's Work"
} 

</script>

<template>
  
  
  <main>


   <h1 @click="changeMsg">{{ msg }}</h1>
   
   <p>Attention, ne dépasse pas les 100 !⚠️</p>

<h2 :class="count < 25 ? 'green' : count < 50 ? 'orange' : 'red'">
  Nombre = {{ count }}
</h2>

   <button @click="incrementCount">Incrémente le compteur</button>
<button
  :style="count <= 0 ? { display: 'none' } : {}"
  @click="resetCount"
>
  Réinitialise le compteur
</button>

  </main>  
  

  </template>

<style scoped>

h1{
  color: rgb(170, 114, 226);

}

h1:hover{
  cursor: pointer;
}

.green { 
  color: green;
}

.orange { 
  color: orange
}

.red {
  color: red
}




</style>
