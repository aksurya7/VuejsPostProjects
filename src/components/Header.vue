<template>
  <div class="hello">
     
    <nav class="navbar navbar-expand-lg navbar-dark mb-3">
  <div class="container">
    <router-link to="/" class="navbar-brand" >{{siteTitle}}</router-link>
  

  <div class="collapse navbar-collapse" id="navbarSupportedContent">
    <ul class="navbar-nav ml-auto">
      <li class="nav-item active">
        <router-link to="/" class="nav-link" >Home <span class="sr-only">(current)</span></router-link> 
      </li>
      <li class="nav-item">
        <router-link to="/about" class="nav-link" >About</router-link>   
      </li>
    </ul>
    
  </div>
  </div>
</nav>
  </div>
</template>

<script>
export default {
  name: 'Header',
  data(){
    return{
      siteTitle: "Vue Basics App"
    }
  }
}
</script>

<style scoped>
.navbar{
  background: #1a1d24;
}

.navbar-nav a{
  color:#fff;
  padding: 0 15px;
  display: block;
}
</style>
