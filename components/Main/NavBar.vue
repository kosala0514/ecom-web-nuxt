<template>
  <nav class="navbar navbar-expand-lg">
    <div class="container-fluid">
      <a class="navbar-brand" href="">Ecom</a>
      <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav" aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="collapse navbar-collapse" id="navbarNav">
        <ul class="navbar-nav">
          <li class="nav-item">
            <a class="nav-link" aria-current="page" href="">Home</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" aria-current="page" href="">Dashboard</a>
          </li>
        </ul>

      </div>
      <div>
        <span><a href="#" class="auth-text"> Login | </a></span>
        <span><a href="#" class="auth-text"> Register</a></span>
    </div>
    </div>
  </nav>
</template>

<script>
  export default{
    name:'NavBar'
  }

</script>
  <style>
    .navbar{
        background-color: #240c37;
    }
    .nav-link, .navbar-brand, .auth-text{
        color: #fff;
    }
    .nav-link:hover, .navbar-brand:hover, .auth-text:hover{
        color: rgb(224, 198, 246);
    }
</style>
