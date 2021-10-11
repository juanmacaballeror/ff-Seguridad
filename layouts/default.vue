<template>
  <div class="container">
    <div class="item item-cabecera">
      <header>
      <h1>
        cabecera
      </h1>
     </header>
    </div>
    <div class="item item-cuerpo">
      <Nuxt/>
    </div>
    <div class="item item-footer">
      <footer>
        <h1>
          footer
          </h1>      
      </footer>
    </div>
  </div>
</template>

<script>
export default {}
</script>

<style lang="scss" scoped>

*,
*::before,
*::after {
    margin: 0;
    padding: 0;
    box-sizing: inherit;
}

html {
    box-sizing: border-box;
    font-size: 62.5%; // 10px/16px = 62.5% -> 1rem = 10px
}

body {
    font-family: $font-primary;
    color: $color-grey-dark-2;
    font-weight: 300;
    line-height: 1.6;
}

.container{
  // width: 100%;
  height: 98vh;
  
  display: grid;
  grid-template-columns: 1fr;
  // grid-template-rows: 1fr 90% 1fr;
  grid-template-rows: auto 1fr auto;

  //justify-items: center;
  //align-items: center;
  // place items center es lo mismo que justify-items: center y align-items: center
  // place-items: center;
   text-align:center;

  // justify-content: center;
    align-content: center;
 
  
  grid-template-areas: "header"
                       "content"
                       "footer";
}

.item{
  border:2px solid black;
  color:white;
}

.item-cuerpo{
  width:85%;
  justify-self: center;
  grid-area:content;
  background-color: yellow;
  // grid-gap: 2rem;
  @media only screen and (max-width: 768px) {
 
    width:100%;
 
  }
}

.item-cabecera{
  grid-area:header;
  background-color:red;
  // grid-gap: 2rem;
}

.item-footer{
  grid-area:footer;
  background-color: blue;
  // grid-gap: 2rem;
}

</style>
