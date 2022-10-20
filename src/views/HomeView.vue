<template>
  <div class="app-container container-fluid">
    <div id="home" class="row hdr-container">
    <div class="row animation_name">
      <div class="col-md-5 col-sm-5 letters" id="letters">
        <div class="nameC" id="letters">C</div>
        <div class="nameL" id="letters">L</div>
        <div class="nameA" id="letters">A</div>
        <div class="nameR" id="letters">R</div>
        <div class="nameA2" id="letters">A</div>
      </div>
      <div class="col-md-2 col-sm-2 ico">
        <i class="bi bi-brightness-low-fill"></i>
      </div>

      <div class="col-md-5 lastName lastname-letters" id="letters">LALIBERTÉ</div>
    </div>

    <div id="button" class="row arrow-ico" @click="displayNavbar" type="button">
      <a href="#about"><i class="bi bi-arrow-down"></i></a>
    </div>
  </div>
  <WhoIAm id="about" />

  <Navbar id="navbar" v-if="revele" />

  <HardSkills id="hardskills" />

  <Experiences id="experiences" />

  <Works id="works" />

  <ContactMe id="contactme"/>
  </div>

</template>

<script>
//Imports
import WhoIAm from "../components/whoIAm.vue";
import HardSkills from "../components/hardSkills.vue";
import Works from "../components/works.vue";
import Experiences from "../components/Experiences.vue";
import Navbar from "../components/Navbar.vue";
import ContactMe from "../components/ContactMe.vue";

export default {
  name: "home",
  components: {
    WhoIAm,
    HardSkills,
    Works,
    Experiences,
    Navbar,
    ContactMe
  },
  data() {
    return {
      revele: false,
    };
  },
  mounted(){
    this.hiddenNavbar()
  },
  methods: {
    displayNavbar() {
      this.revele = true;
    },
    hiddenNavbar() {
      console.log(this.revele); 
      const fadeEffect = document.querySelector('#navbar')
      
      window.addEventListener('scroll', () => { 
        const { scrollTop, clientHeight } = document.documentElement;
        console.log(scrollTop, clientHeight);
        if(scrollTop === 0 && this.revele === true){
          this.revele = false;

        }
      });

    }
  },
};
</script>

<style lang="scss">
#home, #about, #hardskills, #experiences, #works, #contactme{
  height: 100vh;
  @media (max-width: 776px ) {
    height: auto;
  }
}
.hdr-container {
  font-family: "Source Code Pro", monospace;
  display: grid;
  @media (max-width: 776px) {
    align-content: start;
  }
  .animation_name {
    align-items: center;
    align-self: flex-end;
    @media (max-width: 776px){
      align-self: flex-start;
    }
    .ico {
      text-align-last: center;
      font-size: 150px;
    }
    #letters {
      display: flex;
      justify-content: space-between;
      position: relative;
      font-size: 60px;
    }
    .nameC {
      right: -45%;
      opacity: 0;
    }
    .nameL {
      right: -37%;
      opacity: 0;
    }
    .nameA {
      right: -29%;
      opacity: 0;
    }
    .nameR {
      right: -21%;
      opacity: 0;
    }
    .nameA2 {
      right: -13%;
      opacity: 0;
    }
    .lastName {
      opacity: 0;
      text-align-last: center;
      letter-spacing: 25px;
      @media (max-width: 776px){
        letter-spacing: 0px;
      }
    }
  }
  .arrow-ico {
    text-align-last: center;
    align-self: flex-end;
    font-size: 90px;
  }
}
#navbar {
  z-index: 1;
  animation: fadein 2s;
}


@keyframes fadein {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}
@keyframes fadeout {
  from {
    opacity: 1;
  }
  to {
    opacity: 0;
  }
}

.animation_name > .letters > .nameC,
.animation_name > .letters > .nameL,
.animation_name > .letters > .nameA,
.animation_name > .letters > .nameR,
.animation_name > .letters > .nameA2 {
  animation: comeFromRight 1500ms forwards;
  animation-delay: 2s;
}

.animation_name > .ico {
  animation: reducePoint 1000ms forwards;
  animation-delay: 1.5s;
}

.animation_name > .lastName {
  animation: apparitionLname 5000ms forwards;
  animation-delay: 1.5s;
}

@keyframes comeFromRight {
  0% {
  }
  100% {
    opacity: 1;
    right: 0;
  }
}

@keyframes reducePoint {
  0% {
    font-size: 150px;
  }
  100% {
    font-size: 100px;
  }
}

@keyframes apparitionLname {
  0% {
    opacity: 0;
  }
  50% {
    opacity: 50%;
  }
  100% {
    opacity: 1;
  }
}
</style>
