<template>
    <div class="details">
        <h1>country name : {{ locations.name }}</h1>
        <h4> capital : {{ locations.capital }}</h4>
        <p>{{ locations.description }}</p>
        <div class="image">
            <img :src="require(`@/assets/${locations.image}`)" alt="image" />
        </div>
    </div>
</template>

<script>
import store from '@/store.js';
export default {
    name: 'Details',
    props:['name'],
    data(){
        return{
            countryname:this.name,
        };
    },
    computed: {
        locations() {
            return store.location.find(
                location => location.name === this.countryname
            );
        }
    }
}
</script>

<style>
    .details{
        width: 600px;
        margin: 30px 100px;
        color:#fff;
    }
    h1{
        margin: 12px 0;
        color: orange;
        text-transform: capitalize;
    }
    h4{
        margin-bottom: 12px;
        text-transform: capitalize;
    }
    p{
        margin-bottom: 12px;
        line-height: 30px;
        text-transform: capitalize;
    }
    /* .image{
        width: 100%;
    }
    .image img{
        width: 100%;
    } */
</style>