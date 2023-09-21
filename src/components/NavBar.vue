<template>
  <nav class="main-nav">
    <router-link style="color: white; font-weight: bold; font-size: 20px;" :to="{ name: 'HomeView' }">Brandon Chen</router-link> 
    <router-link style="margin-left: 20px" :to="{ name: 'ContactView' }">Contact Me</router-link> 
    <router-link :to="{ name: 'ProjectView' }">Projects</router-link> 
  </nav>
</template>
  
<script>
export default {};
</script>
  
<style>

    .main-nav {
      text-align: left;
      background-color: rgb(31, 41, 55);
    }
    
    .main-nav a {
      display: inline-block;
      text-decoration: none;
      margin: 0 10px;
      color: rgb(156,163,175);
      font-size: 15px;
    }

    nav {
      padding: 15px;
    }

    a.router-link-active {
      color: white;
    }



</style>