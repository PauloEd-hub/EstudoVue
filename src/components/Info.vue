<template>
  <div>
    <p v-if="esta_trabalhando">Estou trabalhando no momento.</p>
    <p v-else>Estou em buscade emprego</p>
    <p>Utilizo as seguintes tecnologias para back-end</p>
    <ul>
      <li v-for="(technology, index) in backend_technologies" v-bind:key="index">{{ technology }}</li>
    </ul>
    <div>
      <button @click="showEmail">Mostrar email</button>
    </div>
    <p v-show="mostrar_email">Mostrar email do cliente: {{ email }}</p>
    <p>
      Para acessar meu portfólio <a v-bind:href="meu_link">basta clicar aqui</a>
    </p>
    <Picture />
  </div>
</template>

<script>
import Picture from "./Picture.vue";
export default {
  name: "Info",
  components: {
    Picture,
  },
  data() {
    return {
      esta_trabalhando: true,
      mostrar_email: false,
      email: "pauloedu.silva@gmail.com",
      meu_link: "https://google.com",
      backend_technologies: ["Java", "Vuejs", "Spring Boot"]
    };
  },
  methods: {
    showEmail() {
      this.mostrar_email = !this.mostrar_email
  },
}
}
</script>
