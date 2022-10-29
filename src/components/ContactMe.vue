<template>
    <div id="contactMe" class="row contact-container">
        
        <div class="container-contact-with-map">
            <ComponentWithMap class="map-image" />
           <div class="row">
                <div class="col-12 col-md-3 content-contact">
                    <div class="title-contact">
                        <p>N'hésitez pas</p>
                        <p class="p-bold">Contactez-moi</p>
                    </div>
                    <div class="details-contact">
                        <p><i class="bi bi-phone"></i>  06 19 04 02 19</p>
                        <p><i class="bi bi-envelope"></i>  Chltpro@gmail.com</p>
                    </div>
                    <div class="btn">
                        <button id="btn" @click="SlideFormContact" type="button" class="btn btn-light">Formulaire de contact</button>
                    </div>
                </div>

                <div class="col-12 col-md-4 content-form form-slide" id="form-slide">
                <div class="contact-form">
                    <form id="form" action="">
                        <h4>Formulaire de contact</h4>
                        <div>
                            <label for="reply_to" class="form-label">Email:</label>
                            <input  v-model="email" type="email" class="form-control" id="reply_to" name="reply_to" placeholder="Laissez moi votre Email" aria-describedby="emailHelp">
                        </div>
                        <div>
                            <label for="message" class="form-label">Votre message:</label>
                            <textarea v-model="message" class="form-control" id="message" name="message" rows="3" placeholder="Je serai ravie de prendre contact avec vous..."></textarea>
                        </div>
                        
                        <div class="button" >
                            <button id="sendBtn" @click="sendEmail()" type="submit" value="Send Email" class="btn btn-light">Envoyer</button>
                        </div>
                    </form>
                </div>
           </div>
           </div>
        </div>
    </div>
</template>

<script>
import emailjs from "emailjs-com"
import ComponentWithMap from './GoogleMaps.vue'

    export default {
        name: "contactMe",
        data(){
            return {
                email: "",
                message: "",
            }
        },
        components: {
            ComponentWithMap,
        },
        methods: {
            SlideFormContact(){
                const btn = document.querySelector('.btn')
                const slide = document.querySelector('.form-slide');
                if(btn.click){
                    slide.classList.add('activeBtn')
                }     
            }, 
            sendEmail() {
                const btn = document.getElementById('sendBtn');

                document.getElementById('form').addEventListener('submit', function(event) {
                    event.preventDefault();
                    
                    btn.innerText = "En cours..."

                    const serviceID = 'service_696tmpa';
                    const templateID = 'template_bhiwqld';
                    const userId = 'OkYb3_3x2XbgyN8aT';
   
                    emailjs.sendForm(serviceID, templateID, this ,userId, {
                        email: this.email,
                        message: this.message
                    }) .then(() => {
                        btn.innerText = 'Email Envoyé';
                        window.location.reload()
                    }, (err) => {
                        btn.innerText = 'Une erreur est survenue';
                    });
                });
            },
        },
     
    }
</script>


<style lang="scss">
.contact-container{
    .container-contact-with-map{
        height: 100vh;
        position: absolute;
        top: 0;
        left: -100px;
        width: 101vw;
        @media (max-width: 776px){
            position: initial;
            width: auto;
        }
        .map-image{
            @media (max-width: 776px) {
                background: none;
            }
        }
        .row{
            align-items: center;
            justify-content: space-evenly;
            .content-contact{
                background: #4a5b71;
                color: white;
                padding: 30px;
                @media (max-width: 776px) {
                    height: 100vh;
                    margin-top: 35px;
                }
                .title-contact{
                    margin-bottom: 50px;
                    font-size: 20px;
                    p{
                        margin: 0;
                    }
                    .p-bold{
                        font-weight: bold;
                        text-transform: uppercase;
                    }
                }
                .btn{
                    button{
                        margin: 20px;
                    } 
                }
            }
            .content-form{
                width: 30%;
                background: #4a5b71;
                color: white;
                padding: 30px;
                height: 100vh;
                display: grid;
                align-content: center;
                h4{
                    font-weight: bold;
                }
                .button{
                    text-align: center;
                    margin: 40px;
                }
                @media (max-width: 776px) {
                    width: 100%;
                    align-content: baseline;
                    height: auto;
            }
        }
           
            .form-slide{
                transform: translateX(500px);
                opacity: 0;
                transition: transform 0.6s ease-in-out,
                opacity 0.6s ease-in-out;
                @media (max-width: 776px){
                transform: matrix(1, 0, 0, 1, 0, 0);
                opacity: 0;
                transition: transform 0.6s ease-in-out,
                opacity 0.6s ease-in-out;
                }
            }
            .form-slide.activeBtn{
                transform: translateX(345px);
                opacity: 1;
                @media (max-width: 1020px){
                    transform: translateX(300px);
                }
                @media (min-width: 1600px){
                    transform: translateX(402px);
                }
                @media (min-width: 1920px){
                    transform: translateX(435px);
                }
                @media (max-width: 776px) {
                    transform: matrix(1, 0, 0, 1, 0, -600);
                    opacity: 1;
                }
                
            }
        }
    }
}

</style>