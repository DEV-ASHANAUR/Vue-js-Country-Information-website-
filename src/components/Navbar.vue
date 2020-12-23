<template>
  <nav>
      <ul>
          <li>
              <router-link to="/">Home</router-link>
          </li>
          <li v-for="location in locations" :key="location.id">
              <router-link :to="{name:'Details',params:{name:location.name}}">{{location.name}}</router-link>
          </li>
      </ul>
  </nav>
</template>

<script>
import store from '@/store.js';
export default {
   name: 'Navbar',
   data(){
       return{
           locations:store.location,
       }
   }
}
</script>

<style>
    nav{
        width: 100%;
        height: 65px;
        padding: 0 100px;
        background: #fff;
        
    }
    nav ul {
        height: 65px;
        display: flex;
        align-items: center;
        list-style: none;
    }
    nav ul li a {
        text-decoration: none;
        padding: 0 15px;
    }
</style>