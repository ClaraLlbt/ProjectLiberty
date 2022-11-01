<template>
<div id="about" class="row row-container">
  <div class="row about-me">
    <div class="col-md-6 profile">
      <div class="image-profile">
        <img src="../assets/images/chibi.png" alt="">        
      </div>
      <div class="row networks-icons">
        <div class="col-4 instagram-icon">
          <a href="https://www.instagram.com/kala__ikebana/"><i class="bi bi-instagram"></i></a>
          <span>Instagram</span>
        </div>
        <div class="col-4 linked-icon">
          <a href="https://www.linkedin.com/in/chltc"><i class="bi bi-linkedin"></i></a>
          <span>LinkedIn</span>
        </div>
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
      </div>
  </div>
  <div class="row btn-HS-discover">
    <div class="col-6 btn">
      <div class="button">
          <button id="buttonHS" class="btn btn-light">
            <a href="#hardskills">Découvrir mes compétences</a>
          </button>
        </div>
    </div>
    <div class="col-6 hobbies-ico">
      <div class="hobbies-container">
          <div class="row hobbies-icons">
            <div class="col-2 icon-1 bubbletitle"><i class="bi bi-brush"></i>
              <span>Painting</span>
            </div>
            <div class="col-2 icon-2 bubbletitle"><i class="bi bi-tools"></i>
              <span>Do-It-Yourself</span>
            </div>
              
            <div class="col-2 icon-3 bubbletitle"><i class="bi bi-cup-hot"></i>
              <span>Coffee Lover</span>
            </div>
            <div  class="col-2 icon-4 bubbletitle"><i class="bi bi-flower1"></i>
              <span>Plant Lover</span>
            </div>
              
            <div class="col-2 icon-5 bubbletitle"><i class="bi bi-code-slash"></i>
              <span>Coding</span>
            </div>
            <div class="col-2 icon-6 bubbletitle"><i class="bi bi-controller"></i>
              <span>Video Games</span>
            </div>
          </div>
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

<style lang="scss">
  .row-container{
    align-content: space-evenly;
    background-image: url("../assets/images/dots-bg.png");
    .about-me{
      align-self: end;
      .profile{
      text-align: center;
      .image-profile{
        text-align-last: center;
        img{
          width: 85%;
        }
      }
      .networks-icons{
        font-size: 40px;
        justify-content: center;
        div{
          a{
            &:hover{
              background: none;
            }
          }
          span{
            border-radius: 5px;
            display: none;
            z-index: 2;
            background: #e7a1b5;
            left: 45px;
            margin: 15px;
            width: 40%;
            position: absolute;
            top: -40px;
            text-decoration: none;
            font-size: 12px;
            color: white;
            font-weight: bold;
          }
          &:hover{
            filter: none;
            cursor: help;
            position: relative;
            span{
              display: block;
            }
          }
        }
      }
    }
    .presentation{
      padding: 20px;
      align-self: center;
      h2{
        font-size: 30px;
        height: 80px;
        margin-bottom: 0;
        @media (max-width: 768px) {
          height: 100%;
        }
        @media (min-width: 1600px){
          font-size: 40px;
          height: 130px;
        }
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
        @media (max-width: 768px) {
          height: 200px;
          overflow: auto;
          font-size: 17px;
        }
        @media (min-width: 1600px){
          font-size: x-large;
        }
      }
    }
    }
  }
  .btn-HS-discover{
    align-content: center;
    @media (max-width: 768px) {
      display: grid;
      justify-items: center;
    }
    .btn, .hobbies-ico{
      align-self: center;
      @media (max-width: 768px) {
        width: 100%;
      }
    }
    .button{
          margin: 20px;
          margin: auto;
          button{
            box-shadow: 1px 0px 6px 0px #4A5B71;
            a{
              font-weight: bold;
              font-size: 18px;
              color: #4A5B71;
              @media (min-width: 1600px){
                font-size: 30px;
              }
            }
          }
        }
        .hobbies-icons{
        font-size: 30px;
        text-align: center;
        padding: 13px;
        div{
          filter:brightness(0.5);
          span{
            border-radius: 5px;
            display: none;
            z-index: 2;
            background: #e7a1b5;
            left: 0;
            margin: 15px;
            width: 120%;
            position: absolute;
            top: -40px;
            text-decoration: none;
            font-size: 12px;
            color: white;
            font-weight: bold;
          }
          &:hover{
            filter: none;
            cursor: help;
            position: relative;
            span{
              display: block;
            }
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
