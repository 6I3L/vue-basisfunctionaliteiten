<template>
  <div id="app">
    <input v-model="product" type="text" placeholder="Voeg een product toe" />
    <button @click="addProduct">Toevoegen</button>
    <ul>
      <li v-for="item in products" :key="item.id">{{ item.name }}</li>
      <li></li> <!-- Leeg list item zoals gevraagd -->
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    return {
      product: "", // Inputveld gelinkt aan variabele product
      products: [], // Lege array voor producten
    };
  },
  methods: {
    addProduct() {
      if (this.product.trim() !== "") {
        this.products.push({ id: Date.now(), name: this.product });
        this.product = ""; // Reset het inputveld na toevoegen
      }
    },
  },
};
</script>

<style>
/* CSS-regels uit het gegenereerde css-bestand */
/* Voeg hier de css-regels toe die je uit het css-bestand hebt gekopieerd */
</style>
