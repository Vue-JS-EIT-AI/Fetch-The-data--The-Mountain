<template>
  <div>

<nav class="navbar navbar-expand-lg navbar-light bg-light">
  <div class="container-fluid">
    <Nuxt-link to="/" class="navbar-brand">Home</Nuxt-link>
    
    <div class="collapse navbar-collapse" id="navbarNav">
      <ul class="navbar-nav">
        <li class="nav-item">
           <Nuxt-link to="/ImgCk" class="nav-link active" aria-current="page">Image Check</Nuxt-link>
        </li>

        <li class="nav-item">
           <Nuxt-link to="/fetch1P" class="nav-link active" aria-current="page">Fetch 1</Nuxt-link>
        </li>

        <li class="nav-item">
           <Nuxt-link to="/fetch2P" class="nav-link active" aria-current="page">Fetch 2</Nuxt-link>
        </li>

         <li class="nav-item">
           <Nuxt-link to="/fetch3P" class="nav-link active" aria-current="page">Fetch 3</Nuxt-link>
        </li>
        
       
      </ul>
    </div>
  </div>
</nav>


    
      <div class="d-flex justify-content-center">
        <Nuxt />   
      </div>
    </div>

</template>

<script>

export default {
  
}
</script>

<style scoped>
.test {
  background-color: rgb(40, 43, 51);
  color: rgb(235, 226, 226);
}
a {
  text-decoration: none;
  color: rgb(15, 13, 13);
}
a:hover{
  color: black;
}



</style>