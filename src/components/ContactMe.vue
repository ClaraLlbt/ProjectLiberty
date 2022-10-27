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
                    <form action="">
                        <h4>Formulaire de contact</h4>
                        <div>
                            <label for="exampleInputEmail1" class="form-label">Email:</label>
                            <input type="email" class="form-control" id="exampleInputEmail1" aria-describedby="emailHelp">
                        </div>
                        <div>
                            <label for="exampleFormControlTextarea1" class="form-label">Votre message:</label>
                            <textarea class="form-control" id="exampleFormControlTextarea1" rows="3"></textarea>
                        </div>
                        
                        <div class="button">
                            <button class="btn btn-light">Envoyer</button>
                        </div>
                    </form>
                </div>
           </div>
           </div>
        </div>
    </div>
</template>

<script>
    import ComponentWithMap from './GoogleMaps.vue'

    export default {
        name: "contactMe",
        components: {
            ComponentWithMap,
        },
        methods: {
            SlideFormContact(){
                const btn = document.querySelector('.btn')
                const slide = document.querySelector('.form-slide');
                if(btn.click){
                    console.log('hello');
                    slide.classList.add('activeBtn')
                }
                
        }
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
                    transform: matrix(1, 0, 0, 1, 0, -405);
                    opacity: 1;
                }
                
            }
        }
    }
}

</style>