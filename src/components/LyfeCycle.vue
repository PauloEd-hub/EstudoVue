<template>
    <h2>Meu nome é: {{ nome }} </h2>
</template>


<script>
export default {
    name: 'LyfeCycle',
    data() {
        return {
            nome: "Ainda não sei"
        }
    },
    created() {
        setTimeout(() => {
             this.nome = "Paulo" 
        }, 1000);
      this.lifeCycle();
    },
    mounted() {
        setTimeout(() => {
            this.nome = "Pedro"

        }, 1000)
        this.lifeCycle();
    },
    methods: {
        lifeCycle() {
            console.log("Executou!!")
        }
    }
}


</script>
