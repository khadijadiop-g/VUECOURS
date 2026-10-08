<script setup>
import { computed, reactive } from 'vue';



// const tab = [1,2,3]
// let s = 0;

// tab.forEach(i => {
//     s=s+i;

// });

// somme = tab.reduce((s,i)=>s+i,0)






const cart = reactive([
    {nom:'Cahier',prix:500,stock:23},
    {nom:'Stylo',prix:400,stock:53},
    {nom:'Livre',prix:2500,stock:40},
    {nom:'Taille',prix:300,stock:13}
]);
const total = computed( function (){
    return cart.reduce((somme,product)=>somme + product.prix* product.stock,0)
});

</script>

<template>
  <section class="card">
    <h2>07 - computed()</h2>

    <ul>
      <li v-for="product in cart" :key="product.nom">
       {{ product.nom }}: {{ product.prix }} × {{ product.stock }} -> {{ product.prix * product.stock }} FCFA
      </li>
    </ul>

    <h3>Total : {{total}} FCFA</h3>

    <p class="note">
      Le total se met à jour automatiquement.
    </p>
  </section>
</template>

<style scoped>
.card { padding:16px; border:1px solid #eee; border-radius:12px; }
.note { margin-top:8px; color:#555; }
</style>