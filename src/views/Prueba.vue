<template>
   <div class="prueba">
     <div class= "container">
      <div class= "row justify-content-center">
        <div class="col-8 md-6">
          <h1>Carrito</h1>
          <ul>
            <li v-for="(item,i) in articulos" :key="i">
              <Item :titulo="item.nombre"
              :descripcion="item.descripcion"
              :imagen="item.imagen"
              :precio="item.precio"
               />
            </li> 
          </ul>
         </div> 
      </div>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src

import {ref} from 'vue'
import Item from '@/components/Item.vue'

export default {
  name: 'Prueba',
  components: {
    
    Item
  },
  setup(){
    const articulos=ref([
      
        {nombre:"llave-fija",descripcion:"numero 2",imagen: require("@/assets/llavefija.jpg"),precio:20.30},
        {nombre:"martillo",descripcion:"carpintero",imagen: require("@/assets/martillo.jpg"),precio:30.50},
        {nombre:"destornillador",descripcion:"plano",imagen: require("@/assets/destornillador.jpg"),precio:13.20} 
      
    ])
    return{
      articulos
    }
}
}
</script>
<style lang="scss">
  li{
    list-style: none;
  }
</style>