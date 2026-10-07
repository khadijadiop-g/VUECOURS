<script setup>
const montant = 900;
const annee = new Date().getFullYear();
const prime = 0.5;
const person = { fullName: "Khadija Rvssul", role: "0stack" };
</script>

<template>
<section class="card">
    <div class="div">Nom: {{ person.fullName }}</div>
    <div class="div">Role: {{ person.role }}</div>
    <div class="div">Montant: {{montant.toLocaleString() }} Fcfa</div>
    <div class="div">Annee: {{annee }}</div>
    <div class="div">Salaire Net: {{montant + montant*prime }}</div>
</section>
</template>



<style scoped >
.card {
  padding: 16px;
  border: 1px solid #eee;
  border-radius: 12px;
}
.div {
  font-size: 2em;
}
</style>