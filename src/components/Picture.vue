<template>
<img :src="avatar" :alt="descricao">


</template>

<script>
export default {
   name: 'Picture',
   data() {
       return{
           avatar: "/img/foto.png",
           descricao: "Matreus Batistis"
       }
   }
}
</script>
