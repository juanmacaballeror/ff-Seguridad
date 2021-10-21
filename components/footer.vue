<template>
  <div class="container-footer">
    <p>FF Seguridad c/ Nueva York 42, local 3, 28936 Móstoles - Madrid</p>


  </div>

</template>

<script>
  export default{
    name:'pie'
  }
 
</script>

<style lang="scss" scoped>
.container-footer{
  padding:1rem;
  display:flex;
  justify-content: center;
  background-image:linear-gradient(to right bottom, $color-grey-dark-1, $color-grey-light-1);
  color:$color-white;
  grid-area:footer;  
}


</style>