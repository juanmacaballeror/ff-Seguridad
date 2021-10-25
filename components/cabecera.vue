<template>
  <div class="contenedor">
      <div class="cabecera cabecera-format">
         <div class="cabecera__tamanio cabecera__rotate">F</div>
         <div class="cabecera__tamanio">F</div> 
         <div>Seguridad</div> 
         <nav class="cabecera__nav">
            <input type="checkbox"  class="cabecera__checkbox"  id="checkbox_toggle" />
            <label for="checkbox_toggle" class="hamburger">&#9776;</label>
            <div class="cabecera__menu">
                <li><a href="#">Sobre nosotros</a></li>
                <li><a href="#">Qué hacemos</a></li>
                <li><a href="#">Nuestros clientes</a></li>
                <li><a href="#">Contacto</a></li>
            </div>
         </nav>
         <!-- <div class="cabecera__header-end"> Nuestro compromiso es su seguridad</div> -->
      </div>    
      <!-- <div class="cabecera__header-end"> Nuestro compromiso es su seguridad</div>            -->
  </div>
</template>
<script>
  export default{
    name:'cabecera'
  }
</script>

<style lang="scss" scoped>

input[type=checkbox]{
  display: none;

  @media only screen and (max-width: 900px) {
    &:checked ~ .cabecera__menu{
      // display: block;
      display: inline-grid;
    }

    // &:checked ~ .hamburger {
    //     background-color: transparent;
    // }

    // &:checked ~ .hamburger {
    //     top: 0;
    //     transform: rotate(135deg);
    // }
    //  &:not(:checked) ~ .hamburger {
    //     top: 0;
    //     //transform: rotate(-135deg);
    // }
   
  }
} 
.hamburger {
  display: none;
  position: relative;
  
  @media only screen and (max-width: 900px) {
      display: block;
      //position:absolute;
      font-size: 2.5rem;
      user-select: none;
  }
}

.contenedor{
 /* Flexbox */
	display:flex;

  background-image:linear-gradient(to right bottom, $color-grey-dark-1, $color-grey-light-1);
  color:$color-white;
  
  grid-area:header;  
}

li {
 list-style: none;

  @media only screen and (max-width: 900px) {
    &:not(:first-child){
      margin-top:4rem;
    }
  }
}

a {
 text-decoration: none;
 color:$color-white;

 &:hover{
   font-size:2rem;
   color: black;
 }

 &:focus{
   color: black;
 }

  @media only screen and (max-width: 900px) {
    font-size:3rem;
  }
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

  &__menu{
    display:flex;
    gap:3rem;
    justify-content: center;
    align-content: center;
    color: $color-white;

     @media only screen and (max-width: 900px) {
        display:none;
        position: absolute;
        background-image:linear-gradient(to right bottom, $color-black, $color-white);
        right: 0;
        left: 0;
        top:6rem;
        text-align: center;
        padding:2rem 0;
        height: 100vh;
    }
  }

  &__nav{
    margin-left: auto;
    font-family: 'Homemade Apple', cursive;
    font-size:1.5rem;
    text-transform: capitalize;
  
 }

  &__rotate{     
    transform: scale(-1, 1);
  }

  &__tamanio{   
    font-size:5rem;
  }

}

</style>