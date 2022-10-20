<template>
  <div id="about" class="row about-me">
    <div class="col-md-6 profile">
      <div class="image-profile">
        <img src="../assets/images/chibi.png" alt="">        
      </div>
        <div class="button">
          <button id="buttonHS" class="btn btn-light">
            <a href="#hardskills">Découvrir mes compétences</a>
          </button>
        </div>
      </div>
      <div class="col-md-6 presentation">
        <h2 id="animate_text"> Hey, je m'appelle Clara et je suis Développeur web Junior</h2>
        <p class="card-txt">
              Je viens d'obtenir mon <b>diplôme.</b>
              Je suis à la <b>recherche</b> d'une expérience professionnelle riche et
              motivante. Je souhaiterais me tourner vers <b>l'alternance</b> dans le
              but de <b>parfaire mes compétences</b> et <b>acquérir de nouveaux savoir.</b>
              Artistique et manuelle, je suis passionnée par le <b>dessin</b> et la
              création.<b>Geek</b>, j’aime allier les nouvelles <b>technologies</b> à <b>l'art.</b>
              C’est pourquoi je cherche à <b>évoluer</b> dans le domaine du <b>développement web</b> 
              afin de pouvoir <b>mettre</b> mes nouvelles <b>compétences à profit</b> dans un environnement 
              de travail <b>en adéquation avec qui je suis.</b>
        </p>
        <div class="hobbies-container">
          <div class="row hobbies-icons">
            <div class="col-2 icon-1"><i class="bi bi-brush"></i></div>
            <div class="col-2 icon-2"><i class="bi bi-tools"></i></div>
              
            <div class="col-2 icon-3"><i class="bi bi-tree"></i></div>
            <div class="col-2 icon-4"><i class="bi bi-flower1"></i></div>
              
            <div class="col-2 icon-5"><i class="bi bi-code-slash"></i></div>
            <div class="col-2 icon-6"><i class="bi bi-controller"></i></div>
          </div>
        </div>
      </div>
  </div>
</template>

<script>
  export default {
    name: "about",
    mounted() {
      this.animateTxt();
    },
    methods: {
      animateTxt() {
        const el = document.getElementById("button");
        el.addEventListener("click", runAnimTxt);
  
        function runAnimTxt() {
          const txt = document.getElementById("animate_text");
          const splitTxt = txt.innerText.split("");
  
          console.log(txt);
  
          txt.innerText = "";
          let i = 0;
          setInterval(function () {
            addLetters();
          }, 100);
          function addLetters() {
            if (i < splitTxt.length) {
              txt.innerHTML += splitTxt[i];
              i++;
            }
          }
        }
      },
      discover(){
         let btnDiscover = document.getElementById('card-right');
         let shadowBox = document.getElementById('profile-card');
         if(btnDiscover.click){
           btnDiscover.style.right = 0;
           btnDiscover.style.left = 'auto'
           shadowBox.style.boxShadow = '0px 0px 5px #744e30';
         }
      }
    },
  };
</script>

<style scoped lang="scss">
  .about-me{
    background-image: url("../assets/images/dots-bg.png");
    .profile{
      text-align: center;
      .image-profile{
        text-align-last: center;
        img{
          width: 85%;
        }
      }
      .button{
          margin: 20px;
          button{
            box-shadow: 1px 0px 6px 0px #4A5B71;
            a{
              font-weight: bold;
              font-size: 18px;
              color: #4A5B71;
            }
          }
        }
    }
    .presentation{
      padding: 20px;
      align-self: center;
      h2{
        margin-bottom: 30px;
        #animate_text:after {
          content: "";
          animation: clignote 0.7s infinite linear;
          width: 2px;
          margin-left: 5px;
          height: 2rem;
          display: inline-block;
          background: rgb(14, 15, 22);
          vertical-align: top;
        }
      }
      p{
        font-size: 19px;
        text-align: justify;
      }
      .hobbies-icons{
        font-size: 30px;
        text-align: center;
        padding: 13px;
        div{
          filter:brightness(0.5);
          &:hover{
            filter: none;
          }
        }
        .icon-1, .icon-3, .icon-5{
          color: #DEBEBE;
        }
        .icon-2, .icon-4, .icon-6{
          color: #E7A1B5;
        }
      }
    }
  }


// KEYFRAMES 

@keyframes clignote {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}
</style>
