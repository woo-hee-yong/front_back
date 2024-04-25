<template>
   <nav class="navbar navbar-expand-md navbar-dark bg-dark">
    <div class="container-fluid" bis_skin_checked="1">
      <!-- <a class="navbar-brand" href="#">Fixed navbar</a> -->
     
      <div class="collapse navbar-collapse" id="navbarCollapse" bis_skin_checked="1">
        <ul class="navbar-nav me-auto mb-2 mb-md-0">
          <li class="nav-item">
            <router-link class="nav-link active" to="/">Why World</router-link>
          </li>
        </ul>
      
        <div class="d-flex" >
            <router-link class="ms-auto link-light p-2" to="/login">Login</router-link>
            <router-link class="ms-auto link-light p-2" to="/signup">SignUp</router-link>
        </div>
      </div>
    </div>
  </nav>
</template>


<script>
    export default{
        
    }
</script>