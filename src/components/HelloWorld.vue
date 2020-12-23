<template>
    <div class="home">
        <h1> Vue js Router </h1>
        <h4></h4>
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Velit reprehenderit esse, architecto labore sapiente sint porro tempore quibusdam obcaecati iusto quae tempora voluptatum dolores, harum neque, delectus corrupti id eveniet?</p>
        <img alt="Vue logo" src="../assets/logo.png">
    </div>
</template>

<script>
export default {
  name: 'HelloWorld',
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  .home{
        width: 600px;
        margin: 30px 100px;
        color:#fff;
    }
    h1{
        margin: 12px 0;
        color: orange;
        text-transform: capitalize;
    }
    p{
        margin-bottom: 12px;
        line-height: 30px;
        text-transform: capitalize;
    }
</style>
