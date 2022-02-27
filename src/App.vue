<template>
  <div>
    <PrimeiroComponent />
    <LyfeCycle />
    <Pessoa />
  </div>
</template>

<script>
import PrimeiroComponent from "./components/PrimeiroComponent.vue";
import LyfeCycle from "./components/LyfeCycle.vue";
import Pessoa from './components/Pessoa.vue'



export default {
  name: "App",
  components: {
    PrimeiroComponent,
    LyfeCycle,
    Pessoa
  },
};
</script>
