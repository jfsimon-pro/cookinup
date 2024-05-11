<script lang="ts">
import SelecionarIngredientes from './SelecionarIngredientes.vue';
import SuaLista from './SuaLista.vue';

export default {
  data() {
    return {
      ingredientes: [] as string[]
    };
  },
  components: { SelecionarIngredientes, SuaLista },
  methods: {
    adicionarIngrediente(ingrediente: string) {
      this.ingredientes.push(ingrediente)
    }
  }
}
</script>

<template>
  <main class="conteudo-principal">
    <SuaLista :ingredientes="ingredientes" />

    <SelecionarIngredientes
    @adicionar-ingrediente="adicionarIngrediente"
    />
  </main>
</template>
