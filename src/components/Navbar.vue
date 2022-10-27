<template>
  <nav id="navbar" class="navbar">
    <div class="container">
      <!-- <a class="navbar-brand" href="#">Logo</a> -->
      <!-- <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
      <span class="navbar-toggler-icon"></span>
    </button> -->
      <div class="navbar-collapse" id="navbarSupportedContent">
        <ul class="navbar-nav me-auto mb-2 mb-lg-0">
          <li class="nav-item">
            <a class="nav-link" aria-current="page" href="#about"
              ><i class="bi bi-person-fill"></i
            ></a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="#hardskills"
              ><i class="bi bi-gear-fill"></i
            ></a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="#experiences"
              ><i class="bi bi-mortarboard-fill"></i
            ></a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="#works"
              ><i class="bi bi-file-earmark-code-fill"></i
            ></a>
          </li>
          <li class="nav-item dettached ">
            <a class="nav-link active" href="#contactme"
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
  @media (max-width:896px) {
    top: -9px;
    width: 106%;
    display: inline-flex;
    left: -12px;
  }
  .container {
    text-align-last: center;
    .navbar-nav{
      background: #F8F8F8;
      display: grid;
      align-content: space-around;
      .nav-item.dettached{
        margin-top: 10px;
        a{
          font-size: x-large;
        } 
      }
      @media (max-width: 896px) {
        display: flex;
        flex-direction: row;
        width: 100%;
        justify-content: space-evenly;
        align-items: center;
        height: 45px;
        .nav-item:nth-child(1){ order: 1; }
        .nav-item:nth-child(2){ order: 2; }
        .nav-item:nth-child(3){ order: 4; }
        .nav-item:nth-child(4){ order: 5; }
        .nav-item:nth-child(5){ order: 3; }
      }
    }
  }

  @media (min-width: 1600px){
    width: 8%;
    .navbar-nav{
      height: 30vh;
      a{
        font-size: x-large;
      }
    }
  }
}
</style>
