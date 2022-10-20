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

        <div type="" class="arrow">
          <a href="#contactme"><i class="bi bi-caret-down"></i></a>
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
    .content-projects{
      p{
        font-weight: bold;
      }
    }
    .projects{
      height: 85vh;
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
                }
                i{
                  font-size: 40px;
                }
              }
            }
          }
        }
        .carousel-indicators{
          margin-bottom: 0px;
        }
      }
      #verticalCarousel{
            border: 35px rosybrown solid;
            overflow: hidden;
            height: 66vh;
            figure{
              position: relative;
              width: 100%;
              margin: 0;
              top: 0;
              text-align: center;
              animation: 15s slidy infinite; 
             
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
