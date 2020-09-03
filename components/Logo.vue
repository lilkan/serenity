<template>
 <h1>hello</h1>

</template>
<script>

  export default {
    data(){
      return{
        msg: ''
      }
    },
    async created(){
      try {
        const res = await this.$axios.$get("http://localhost:3000/posts");
        console.log(res);
        this.msg = res;
        console.log(res.data)
      } catch (e) {
        console.error(e)
      }
    }
  }
</script>
<style lang="scss" scoped>
h1 {
  font-size: 25px
}
</style>
