<template>
  
    <div class="item row">
      <div class="col-1">
          <img :src="imagen">
      </div> 
      <div class="col-11">
        <h3 v-html="titulo"></h3>
        <p v-text="descripcion"></p>
        <h3>Total:</h3>
        <h2 v-text="total"></h2>
        Unidades:
        <input v-model="cantidad" size="5" type="number">
      </div> 
      <hr>
   </div>
 
</template>

<script>
import {ref,computed} from 'vue'
export default {
  name: 'Item',
  props: {
      imagen: String,
      titulo:String,
      descripcion:String,
      precio:Number,
      
  },

  setup(props){
      let cantidad=ref(1)
      let total= computed(()=>{
         return (props.precio*cantidad.value).toFixed(2)

      })
      return{
          cantidad,
          total
      }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
img{
    max-width: 80px;
    margin-bottom: 10px;
    border: orange solid 2px;
}

</style>