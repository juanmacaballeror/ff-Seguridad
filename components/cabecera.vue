<template>
  <div class="contenedor">
      <div class="cabecera cabecera-format">
         <div class="cabecera__tamanio cabecera__rotate">F</div>
         <div class="cabecera__tamanio">F</div> 
         <div class="cabecera__seguridad">Seguridad</div> 
         <div class="cabecera__header-end"> Nuestro compromiso es su seguridad</div>
      </div>  
       
  </div>
</template>
<script>
  export default{
    name:'cabecera'
  }
</script>

<style lang="scss" scoped>

.contenedor{
 /* Flexbox */
	display:flex;

  background-image:linear-gradient(to right bottom, $color-grey-dark-1, $color-grey-light-1);
  color:$color-white;
  
  grid-area:header;  
}

.cabecera{
  /* Flexbox */
  width: 100%;
	display: flex;

  font-family: "Cabin Sketch";
  
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

  &__seguridad{
   //margin-top:1rem;
  }

  &__header-end{
    margin-left: auto;
    // font-family:'Styles';
    font-size:1.5rem;
    text-transform: capitalize;
  }
}


</style>