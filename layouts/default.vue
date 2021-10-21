<template>
  <div class="container">
    <app-cabecera></app-cabecera>
    <div class="item item-cuerpo">
      <Nuxt/>
    </div>
    <app-footer></app-footer>
  </div>
</template>

<script>
export default {}
</script>

<style lang="scss">

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
  height: 100vh;
  
  display: grid;
  grid-template-columns: 1fr;
  grid-template-rows: auto 1fr auto;
  text-align:center;
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
    heigth:100%;
  }
}

</style>
