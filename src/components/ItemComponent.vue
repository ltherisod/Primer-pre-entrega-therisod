<template>
  <div class="card m-3" style="width: 18rem;">
  <div class="image card-img-top" v-bind:style="{'background-image': 'url(' + prod.img + ')' }"></div>
  <div class="card-body">
    <h5 class="card-title">{{prod.name}}</h5>
    <p class="card-text">$ {{prod.price}}</p>
  </div>
    <button  @click="goThere({path:`/detail/${prod.id}`})" class="btn btn-dark">Check it out!</button>
</div>
</template>

<script>
export default {
  name: 'ItemComponent',
    props:{
        prod:Object
    },
    methods: {
        goThere(url){
            this.$router.push(url);
        }
    },
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
    .image{
        background-size:cover;
        width:100%;
        height:18rem;
    }
</style>
