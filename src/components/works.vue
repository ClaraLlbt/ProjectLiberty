<template>
  <div id="projects-container" class="row works-container">

    <div class="row global-row">
      <!-- About Projects -->
      <div class="col-md-3 about-projects">

        <div class="content-projects">
          <h3>Projets</h3>
          <p>Je vous présente les projets que j'ai réalisé lors de ma formation de Développeur Web
            Si vous souhaitez en discuter, je vous propose de me contacter.
          </p>
        </div>

      </div>

      <!-- Projects Bloc -->
      <div class="col-md-9 projects">
        <!-- Bootstrap Horizontal Carousel  -->
        <div  id="horizontalCarousel" class="carousel carousel-horizontal carousel-dark" data-bs-ride="false">
          <!--Carousel indicators-->

          <!--Horizontal Carousel content-->
          <div class="carousel-inner horizontal">
            

            <!--Carousel Projects Items-->
            <div class="carousel-item horizontal active">
              <div class="row project-row">
                <div class="col-6 col-carousel">
                  <!--CSS Carousel Vertical-->
                  <div id="verticalCarousel" class="carousel vertical slide">
                    <figure>
                      <img src="../assets/images/carousel/logo_reservia.png" class="w-100" alt="">
                      <img src="../assets/images/carousel/reservia_page.png" class="w-100" alt="">
                      <img src="../assets/images/carousel/responsive_version.png" class="w-100" alt="">
                    </figure>
                  </div>
                </div>
                <div class="col-6 col-about-project">
                  <div class="title-project">
                    <h6>- PROJET 1 -</h6>
                    <p>Transformer une maquette en site Web avec HTML & CSS</p>
                  </div>
                  <div type="" class="arrow-link">
                    <a href="https://clarahlt.github.io/HaultcoeurClara-2-02112020/"><p>Découvrir</p> 
                      <i class="bi bi-link"></i>
                    </a>
                  </div>
                </div>
              </div>

            </div>
            <div class="carousel-item horizontal">
              <div class="row project-row">
                <div class="col-6 col-carousel">
                  <!--Carousel Vertical-->
                  <div id="verticalCarousel" class="carousel vertical slide">
                    <figure>
                      <img src="../assets/images/carousel/logo_ohmyfood.png" class="w-100" alt="">
                      <img src="../assets/images/carousel/ohmyfood_p1.png" class="w-100" alt="">
                      <img src="../assets/images/carousel/ohmyfood_p2.png" class="w-100" alt="">
                    </figure>
                  </div>
                </div>
                <div class="col-6 col-about-project">
                  <div class="title-project">
                    <h6>- PROJET 2 -</h6>
                    <p>Dynamiser une page web avec des animations CSS</p>
                  </div>
                  <div type="" class="arrow-link">
                    <a href="https://clarahlt.github.io/HaultcoeurClara-3-28022020/"><p>Découvrir</p> 
                      <i class="bi bi-link"></i>
                    </a>
                  </div>
                </div>
              </div>

            </div>
            <div class="carousel-item horizontal">
              <div class="row project-row">
                <div class="col-6 col-carousel">
                  <!--Carousel Vertical-->
                  <div id="verticalCarousel" class="carousel vertical slide">
                    <figure>
                      <img src="../assets/images/carousel/logo_orinoco.png" class="w-100" alt="">
                      <img src="../assets/images/carousel/orinoco_p1.png" class="w-100" alt="">
                      <img src="../assets/images/carousel/orinoco_p2.png" class="w-100" alt="">
                    </figure>
                  </div>
                </div>
                <div class="col-6 col-about-project">
                  <div class="title-project">
                    <h6>- PROJET 3 -</h6>
                    <p>Construire un site E-commerce</p>
                  </div>
                  <div type="" class="arrow-link">
                    <a href="https://clarahlt.github.io/Orinoco/"><p>Découvrir</p> 
                      <i class="bi bi-link"></i>
                    </a>
                  </div>
                </div>
              </div>

            </div>
            <div class="carousel-item horizontal" >
              <div class="row project-row">
                <div class="col-6 col-carousel">
                  <!--Carousel Vertical-->
                  <div id="verticalCarousel" class="carousel vertical slide">
                    <figure>
                      <img src="../assets/images/carousel/logo_piquante.png" class="w-100" alt="">
                      <img src="../assets/images/carousel/piquante_p1.png" class="w-100" alt="">
                      <img src="../assets/images/carousel/piquante_p2.png" class="w-100" alt="">
                    </figure>
                  </div>
                </div>
                <div class="col-6 col-about-project">
                  <div class="title-project">
                    <h6>- PROJET 4 -</h6>
                    <p>Construire une API sécurisée oour une application</p>
                  </div>
                  <div type="" class="arrow-link">
                    <a href="https://clarahlt.github.io/PIIQUANTE/"><p>Découvrir</p> 
                      <i class="bi bi-link"></i>
                    </a>
                  </div>
                </div>
              </div>

            </div>
            <div class="carousel-item horizontal" >
              <div class="row project-row">
                <div class="col-6 col-carousel">
                  <!--Carousel Vertical-->
                  <div id="verticalCarousel" class="carousel vertical slide">
                    <figure>
                      <img src="../assets/images/carousel/logo_groupomania.png" class="w-100" alt="">
                      <img src="../assets/images/carousel/groupomania-p1.png" class="w-100" alt="">
                      <img src="../assets/images/carousel//groupomania_p2.png" class="w-100" alt="">
                    </figure>
                  </div>
                </div>
                <div class="col-6 col-about-project">
                  <div class="title-project">
                    <h6>- PROJET 5 -</h6>
                    <p>Créer un réseau social d'entreprise</p>
                  </div>
                  <div type="" class="arrow-link">
                    <a href="https://clarahlt.github.io/HaultcoeurClara-2-02112020/"><p>Découvrir</p> 
                      <i class="bi bi-link"></i>
                    </a>
                  </div>
                </div>
              </div>

            </div>
            
            
          </div>

          <!--Btn preview/next-->
          <button class="carousel-control-prev" type="button" data-bs-target="#horizontalCarousel" data-bs-slide="prev">
            <span class="carousel-control-prev-icon" aria-hidden="true"></span>
            <span class="visually-hidden">Previous</span>
          </button>
          <button class="carousel-control-next" type="button" data-bs-target="#horizontalCarousel" data-bs-slide="next">
            <span class="carousel-control-next-icon" aria-hidden="true"></span>
            <span class="visually-hidden">Next</span>
            </button>
        </div>

      </div>


      <div type="" class="arrow">
          <a href="#contactme"><i class="bi bi-caret-down"></i></a>
        </div>
    </div>
  </div>
</template>


<script>


export default {
  name: "works",
  mounted(){

  },
  methods:{
  
  }
};
</script>

<style lang="scss">
.works-container {
  .global-row {
    align-self: center;
    align-items: center;
    width: 100vw;
    margin: auto 15px;
    .about-projects{
      @media (max-width: 780px) {
      padding-top: 60px;
    }
    }
    .content-projects{
      p{
        font-weight: bold;
        @media (max-width: 768px) {
          font-size: small;
        }
      }
    }
    .projects{
      height: 85vh;
      @media (max-width: 780px) {
        height: auto;
      }
      #horizontalCarousel{
        height: 100%;
        .carousel-inner.horizontal{
          .carousel-item.horizontal{
            .project-row{
              align-items: center;
              text-align-last: center;
              width: 80%;
              height: 85vh;
              margin: auto;
              @media (max-width: 768px) {
                display: grid;
                justify-items: center;
                align-items: flex-start;
                height: fit-content;
                .col-carousel, .col-about-project{
                  width: 100%;
                }
                .col-about-project{
                  @media (max-width: 780px) {
                    .title-project{
                      text-align-last: justify;
                    }
                  }
                }
              }
              h6{
                font-weight: bold;
                font-size: 25px;
                color: rosybrown;
              }
              p{
                font-weight: bold;
              }
              .arrow-link{
                p{
                  margin-bottom: -20px;
                  font-size: 30px;
                  @media (max-width: 780px) {
                    font-size: 20px
                  }
                }
                i{
                  font-size: 40px;
                }
              }
            }
          }
          
        }
        button{
          @media (max-width: 780px) {
            height: 60%;
          }
        }
      }
      #verticalCarousel{
            border: 35px rosybrown solid;
            overflow: hidden;
            height: 415px;
            @media (max-width: 1020px){
              height: 300px;
              border: 10px rosybrown solid;
            }
            @media (min-width: 1023px){
              height: 325px;
              border: 10px rosybrown solid;
            }
            @media (min-width: 1280px){
              height: 425px;
              border: 10px rosybrown solid;
            }
            @media (min-width: 1600px){
              height: 480px;
              border: 35px rosybrown solid;
            }
            @media (min-width: 1680px){
              height: 492px;
              border: 35px rosybrown solid;
            }
            @media (min-width: 1920px){
              height: 567px;
              border: 35px rosybrown solid;
            }
            @media (max-width: 280px){
              height: 225px;
              border: 10px rosybrown solid;
            }
            @media (min-width: 320px) and (max-width: 375px) {
              height: 305px;
              border: 10px rosybrown solid;
            }
            @media (min-width: 390px) and (max-width: 420px) {
              height: 330px;
              border: 10px rosybrown solid;
            }
            figure{
              position: relative;
              width: 100%;
              margin: 0;
              top: 0;
              text-align: center;
              animation: 15s slidy infinite; 
              @media (min-width: 280px) and (max-width: 1023px){
                animation: none;
                img{
                display: none;
                }
                img:nth-child(1) { display: block}
              }

            }
        }
        @keyframes slidy {
0% { top: 0%; }
30% { top: 0%; }
35% { top: -102%; }
45% { top: -102%; }
50% { top: -102%; }
70% { top: -102%; }
75% { top: -204%; }
95% { top: -204%; }
100% { top: -204%; }
}

    }
  }
}
</style>
