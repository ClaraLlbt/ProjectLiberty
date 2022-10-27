<template>
    <div id="hardskills" class="row hardskills-container">
      <div class="row" id="skills">
        <div class="row development bloc-1">
          <div class="col-md-4 code-icon icon-1">
            <i id="icon1-color" class="bi bi-code"></i>
          </div>
          <div class="col-md-8 dev-skills" data-mdb-animation-on-scroll="repeat">
            <h4 id="icon1-color">Développement</h4>
            <div class="row">
              <div class="col-6">
                <h5>Backend</h5>
                <p>SQL</p>
                <p>SEO</p>
                <p>API REST</p>
                <p>ExpressJS</p>
              </div>
              <div class="col-6">
                <h5>Frontend</h5>
                <p>HTML/CSS/Bootstrap/Sass</p>
                <p>NodeJS</p>
                <p>Javascript</p>
                <p>angularJS/Vuejs</p>
              </div>
            </div>
          </div>
        </div>

        <div class="row development bloc-2">
          <div class="col-md-8 dev-skills">
            <h4 id="icon2-color">Design</h4>
            <p>Clip Studio Paint</p>
            <p>Adobe Illustrator/Indesign/Photoshop</p>
          </div>
          <div class="col-md-4 code-icon" id="icon2-color">
            <i class="bi bi-palette2"></i>
          </div>
        </div>

        <div class="row development bloc-3">
          <div class="col-md-4 code-icon" id="icon3-color">
            <i class="bi bi-code"></i>
          </div>
          <div class="col-md-8 dev-skills">
            <h4 id="icon3-color">Environnement de travail</h4>
            <p>IDE : Visual Studio Code</p>
            <p>Workflow : Github</p>
            <p>Bureautique : Google Drive/Microsoft Office/Libre Office</p>
          </div>
        </div>
        <div class="row arrow" type="">
          <a href="#experiences"><i class="bi bi-caret-down"></i></a>
        </div>
      </div>
    </div>
</template>

<script>
export default {
  name: "hardskills",
  mounted() {
    this.slideBloc()
  },
  methods: {
    slideBloc(){
      const blocSlide1 = document.querySelector('.bloc-1');
      const blocSlide2 = document.querySelector('.bloc-2');
      const blocSlide3 = document.querySelector('.bloc-3');

      window.addEventListener('scroll', () => { 
        const { scrollTop, scrollHeight ,clientHeight} = document.documentElement;
        const topElementToTopViewport = blocSlide1.getBoundingClientRect().top
        if(scrollTop > (scrollTop + topElementToTopViewport).toFixed() - clientHeight * 0.30){
          blocSlide1.classList.add('active');
          blocSlide2.classList.add('active2');
          blocSlide3.classList.add('active3')
        }
      });

    }
  } 
}
</script>

<style lang="scss">
.hardskills-container {
  align-content: center;
  padding: 30px 50px 0px 50px;
  @media (max-width: 776px) {
    padding: 0px;
  }
}
#skills {
  height: 100%;
  margin: 10px;
  #icon1-color {
    color: #396CF1;
  }
  #icon2-color {
    color: #f89b3b;
    i{
      font-size: 70px;
    }
  }
  #icon3-color {
    color: #F853B8;
  }
  .development {
    .code-icon {
      align-self: center;
      text-align: center;
      font-size: 100px;
    }
    .dev-skills {
      padding: 15px;
      background: #F8F8F8;
      border-radius: 10px;
      align-self: center;
      h5,h4 {
        font-weight: bold;
      }
      p {
        margin-bottom: 0;
        font-weight: bold;
        @media (max-width: 776px){
          overflow-wrap: break-word;
          font-size: 12px;
        }
      }
    }
  }
  .bloc-1{
    transform: translateX(-100%);
    opacity: 0;
    transition: transform 2s ease-in-out,
    opacity 0.6s ease-in-out;
  }
  .bloc-1.active{
    transform: translateX(0%);
    opacity: 1;
  }
  .bloc-2{
    transform: translateX(120%);
    opacity: 0;
    transition: transform 2s ease-in-out,
    opacity 0.6s ease-in-out;
    @media (max-width: 776px){
      flex-direction: column-reverse;
    }
  }
  .bloc-2.active2{
    transform: translateX(0%);
    opacity: 1;
  }
  .bloc-3{
    transform: translateX(-100%);
    opacity: 0;
    transition: transform 2s ease-in-out,
    opacity 0.6s ease-in-out;
  }
  .bloc-3.active3{
    transform: translateX(0%);
    opacity: 1;
  }
}
.arrow {
  text-align: center;
  align-content: center;
  margin-top: -10px;
  a {
    &:hover {
      background-color: unset;
    }
    i {
      font-size: 50px;
      &:hover {
        background-color: hsla(160, 100%, 37%, 0.2);
      }
      @media (min-width: 1600px){
        font-size: 100px;
      }
    }
  }
}
</style>
