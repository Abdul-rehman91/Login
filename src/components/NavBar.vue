<template>
<nav class="navbar navbar-expand-lg " id="navbar">
  <div class="container-fluid">
    <a class="navbar-brand" href="#">
      <img src="../assets/9269296-illustration-of-logo-on-white-background.jpg" img-fluid alt="">
    </a>
    <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav" aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
      <span class="navbar-toggler-icon"></span>
    </button>
    <div class="collapse navbar-collapse" id="navbarNav">
      <ul class="navbar-nav">
        <li class="nav-item">
          <a class="nav-link active" aria-current="page" href="#">Home</a>
        </li>
        <li class="nav-item ">
          <a class="nav-link " href="#">Sign In</a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="#">Sign Up</a>
        </li>
       </ul>
    </div>
     
  </div>
</nav>
</template>

<script>
export default {
    name:'NavBar',
}
</script>

<style>
.navbar-brand img{
    width: 60px;
    height: auto;
}
#navbar{
 
  background-color: black;
}
#navbar a{
  color: white;
}
.navbar-toggler{
  
  background-color: white;
}
</style>