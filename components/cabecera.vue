<template>
  <div>
    <header>
      <div class="cabecera cabecera-format">
         <div class="cabecera__tamanio cabecera__rotate">F</div>
         <div class="cabecera__tamanio cabecera__secondF">F</div> 
         <div class="cabecera__seguridad">Seguridad</div> 
      </div>         
    </header>
  </div>
</template>
<script>
  export default{
    name:'cabecera'
  }
</script>

<style lang="scss" scoped>

.cabecera{
  display:flex;
  flex-wrap: nowrap;
  justify-content:flex-start;
  align-items: flex-end;
  align-content:flex-end;
  grid-area:header;
  background-image:linear-gradient(to right bottom, $color-grey-dark-1, $color-grey-light-1);
  color:$color-white;
  font-family: "Cabin Sketch";
  // position:relative;
  
  &-format{
      padding:2rem;
      text-transform: uppercase;
      letter-spacing: 2px;
      line-height: 24px;
      font-size:2rem;
  }

   &__rotate{
     transform: scale(-1, 1);
   }
   &__tamanio{
      font-size:5rem;
   }

  //  &__seguridad{
  //    margin-top:1rem;
  //  }
  
  
}

</style>