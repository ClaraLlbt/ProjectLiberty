<template>
  <nav id="navbar" class="navbar">
    <div class="container">
      <!-- <a class="navbar-brand" href="#">Logo</a> -->
      <!-- <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
      <span class="navbar-toggler-icon"></span>
    </button> -->
      <div class="navbar-collapse" id="navbarSupportedContent">
        <ul class="navbar-nav me-auto mb-2 mb-lg-0">
          <li class="nav-item bg-light">
            <a class="nav-link active" aria-current="page" href="#about"
              ><i class="bi bi-person-fill"></i
            ></a>
          </li>
          <li class="nav-item bg-light">
            <a class="nav-link" href="#hardskills"
              ><i class="bi bi-gear-fill"></i
            ></a>
          </li>
          <li class="nav-item bg-light">
            <a class="nav-link" href="#experiences"
              ><i class="bi bi-mortarboard-fill"></i
            ></a>
          </li>
          <li class="nav-item bg-light">
            <a class="nav-link" href="#works"
              ><i class="bi bi-file-earmark-code-fill"></i
            ></a>
          </li>
          <li class="nav-item dettached bg-light">
            <a class="nav-link" href="#contactMe"
              ><i class="bi bi-envelope-paper"></i>
            </a>
          </li>
        </ul>
      </div>
    </div>
  </nav>

</template>

<script>
export default {
  name: "Navbar",
};
</script>

<style lang="scss">
.navbar {
  width: 6%;
  position: fixed;
  top: 30vh;
  left: 0;

  .container {
    text-align-last: center;
    .nav-item.dettached{
      margin-top: 10px;
      a{
        font-size: x-large;
      }
    }
  }
}
</style>
