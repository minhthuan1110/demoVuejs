
<template>
    <div class="slider">
        <carousel >
            <carousel-slide v-for="slide in slides" :key="slide" class="carousel-slider">
                <img :src="slide" :alt="slide">
            </carousel-slide>
        </carousel>
        <div class="caption">
            <a href="" class="caption__link">
                <span class="caption-text">FLash sale</span>
                <h2 class="caption_title">Summer Collecton</h2>
                <a href="" class="btn-link">shop now 
                    <span>
                        <i class="las la-long-arrow-alt-right"></i>
                    </span>
                </a>
            </a>
        </div>
    </div>    
</template>

<script>
import Carousel from './Carousel.vue';
import CarouselSlide from './CarouselSlide.vue';
export default {
    data(){
        return {
            slides: [
                'https://cdn.shopify.com/s/files/1/0326/6517/4152/files/Slideshow-img-fixed_1728x.jpg?v=1623902209',
                'https://cdn.shopify.com/s/files/1/0326/6517/4152/files/Slideshow-2_1728x.jpg?v=1623838645',
                'https://cdn.shopify.com/s/files/1/0326/6517/4152/files/Slideshow-3_1728x.jpg?v=1623838645',
            ],    
        }
    },
    components : {
        Carousel : Carousel,
        CarouselSlide : CarouselSlide,
    }
}
</script>

<style >
   
    .slider {
        display:flex;
        justify-content: center;
        position:relative;
    }
    .carousel {
        /* position:relative; */
        overflow: hidden;
        width:100%;
        height:auto;
        z-index:10;
    }
    .slider:hover .btn {
        opacity: 1;
        transform: scale(.7);
        transition-property: all;
        transition-duration: 0.2s;
        transition-timing-function: ease-in-out;
        transition-delay: 0s;
    }

    .btn {
        opacity: 0;
        transform: scale(.1);
        background: #fff;
        color: rgb(131, 121, 121);
        border-color: rgb(202, 200, 200);
        box-shadow: 0 0 3px 0 rgb(0 0 0 / 20%);
        position:absolute;
        margin-top:-25px;
        cursor: pointer;
        border: 1px solid rgb(255, 255, 255);
        padding: 15px 20px;
        font-size: 16px;
        font-weight: 600;
        min-height: 40px;
        z-index:20;
    }
    .btn:hover {
        cursor: pointer;
        background-color:red;
        color: #fff;
    }
    .btn:focus{
        outline:none;
    }
    .btn-next {
        top:50%;
        right:0;
        z-index:10;
        
    }
    .btn-prev {
        top:50%;
        left:0;
        z-index:10;
      
    }

    .btn-next i ,
    .btn-prev i {
        font-size:25px;
    }
    .carousel-slider {
        /* position:absolute; */
        /* top:0;
        left:0;
        bottom:0;
        right:0; */
        width: 100%;
        max-height: 110vh;
    }
    .caption {
        position:absolute;
        z-index: 10;
        top:0;
        left:7.3%;
        bottom:0;
        right:5%;
    }
    .caption__link {
        display: flex;
        width:100%;
        height:100%;
        flex-direction: column;
        justify-content: center;
        padding-left: 10%;
        text-decoration: none;

    }
    .caption-text {
        font-size: 18px;
        margin-bottom: 18px;
        font-weight: 400;
        color: #ffffff;
        font-family: 'Inter', sans-serif;
        text-transform: uppercase;
   }
    .caption__link .btn-link {
        font-family: 'Inter', sans-serif;
        text-decoration: none;
        text-transform: uppercase;
        display: inline-flex;
        -ms-flex-align: center;
        align-items: center;
        -ms-flex-pack: center;
        justify-content: center;
        margin-bottom: 5px;
        padding-left: 40px;
        padding-right: 40px;
        border-radius: 0px;
        font-weight: 400;
        min-height: 50px;
        max-width: 180px;
        font-size: 13px;
        color: #ffffff;
        cursor: pointer;
        border: 2px solid #222;
        padding: 5px 20px;
        background-color: #000000;
        border-color: #000000;
        z-index: 10;
    }
    .caption__link .btn-link span {
        margin-left:5px;
        font-size:16px;
    }

    .caption__link .btn-link:hover .btn-link span {
        margin-left:15px;
    }

    .caption_title {
        font-size: 65px;
        margin-top: -15px;
        /* margin-bottom: 5px; */
        font-weight: 600;
        color: #ffffff;
        font-family: Poppins;
    }
    .carousel-slider img {
        width:100%;
        height:100%;
        animation: zom 4s  ;
        -moz-animation: zom 4s   ;
        -webkit-animation: zom 4s   ;
        -o-animation: zom 4s  ;
        transform: scale(1)
        
    }
    @keyframes zom {
        0% {
            transform: scale(1.2);
            opacity:0
        }
        25% {
            opacity:1 ;
        }
        100% {
            transform: scale(1);
        }
    }
</style>
