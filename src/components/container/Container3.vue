<template>
    <div class="container3" >
        <div class="container3-r grid wide">
            <div class="container3-content row no-gutters">
                <div class="container_content-left  l-6 m-12 c-12" >
                    <div class="content-animated">
                        <h4 class="animate_title-time">
                            SPRING - SUMMER 2021
                        </h4>
                        <h2 class="animate__title">
                            Lookbook Collection
                        </h2>
                        <p class="animate_text">After many months design and development raking over
                            every detail of what a modern online retailer needs, Kalles is ready
                            to take your online empire to the next level.
                        </p>
                        <a href="" class="btn-link">shop now 
                            <span>
                                <i class="las la-long-arrow-alt-right"></i>
                            </span>
                        </a>
                    </div>
                </div>
                <div class="container_content-right  l-6 m-12 c-12">
                    <div class="animate-picter">
                        <img src="https://cdn.shopify.com/s/files/1/0326/6517/4152/files/lookbook-img-3_360x.png?v=1623912567" alt="">
                    </div>
                    <div class="icon_show-product" v-for="(product , index) in products" :key="index">
                        <div class="animate-icon" @click="hendleChecked(index)">
                            <i class="fas fa-plus"></i>
                        </div>
                        <div class="show__product-review " :class="{active:checked === index}">
                            <div class="container_content-product">
                                <div class="sale-product-imgs">
                                    <a href="" class="sale-product-imglink">
                                        <img :src="product.image"  alt="" class="sale-product-img">
                                    </a>
                                    <a href="" class="sale-product-imglink"> 
                                        <img :src="product.img2" alt="" class="sale_product-img-after">
                                    </a>
                                    <div class="list-icons">
                                        <a href="" class="icon-link  " title="Add to Wishlist">
                                            <span class="icon-tile-hert">
                                                <i class="far fa-heart"></i>
                                            </span>
                                            <span class="icon-tile-active">
                                                <i class="fas fa-heart"></i>
                                            </span>
                                        </a>
                                        <a href="" class="icon-link  " title="Compare">
                                                <span class="icon-tile-sync">
                                                <i class="las la-sync"></i>
                                            </span>
                                            <span class="icon-tile-sync-active">
                                                <i class="las la-sign-in-alt"></i>
                                            </span>
                                        </a>
                                    </div>
                                    <div class="sale-product-btn">
                                        <a href="" class="item-btn-link" title="Quick view">
                                            <i class="far fa-eye"></i>
                                        </a>
                                        <a href="" class="item-btn-link" title="Add to cart">
                                            <i class="fas fa-shopping-cart"></i>
                                        </a>     
                                    </div>
                                    <div class="discount_product">
                                        <span>{{percentage(product.price,product.priceDiscount)}} %</span>
                                    </div>
                                </div>
                                <div class="sale_product-item-title">
                                    <a href="" class="sale_product-link">{{product.nameProduct}}</a>
                                    <span class="sale_product-price sale">
                                        {{product.price}}
                                    </span>
                                    <span class="sale_product-price saled">
                                        {{product.priceDiscount}} 
                                    </span>
                                </div>         
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
            <div class="moldal--show" v-show="isCondition" @click="isCondition=false">
                <div class="modal-show_sidebar"  >
                    <div class="modal-close" >
                        <i class="fas fa-times" @click="isCondition= false"></i>
                    </div>
                        <div class="moldal" v-show="isCondition" @click="checked=''">   
                    </div>
                </div>
            </div>
        </div>
</template>
<script type="text/javascript">

        
export default {
    data () {
        
        return {
            isCondition:false,
            checked: '',
            products: [
                {
                    image:'https://cdn.shopify.com/s/files/1/0326/6517/4152/products/11_360x.jpg?v=1623831496',
                    img2:'https://cdn.shopify.com/s/files/1/0326/6517/4152/products/191_360x.jpg?v=1623831575',
                    nameProduct:'Ripped Distressed Top',
                    price: 3600,
                    priceDiscount:1500
                },
                {
                    image:'https://cdn.shopify.com/s/files/1/0326/6517/4152/products/191_360x.jpg?v=1623831575',
                    img2:'https://cdn.shopify.com/s/files/1/0326/6517/4152/products/193_360x.jpg?v=1623831576',
                    nameProduct:'Milkmaid Shirred Top',
                    price: 3100,
                    priceDiscount:1100
                },
                {
                    image:'https://cdn.shopify.com/s/files/1/0326/6517/4152/products/41_360x.jpg?v=1623831641',
                    img2:'	https://cdn.shopify.com/s/files/1/0326/6517/4152/products/42_360x.jpg?v=1623831642',
                    nameProduct:'Ruched Bust Sports',
                    price: 3900,
                    priceDiscount:2400
                },
                {
                    image:'https://cdn.shopify.com/s/files/1/0326/6517/4152/products/41_360x.jpg?v=1623831641',
                    img2:'	https://cdn.shopify.com/s/files/1/0326/6517/4152/products/42_360x.jpg?v=1623831642',
                    nameProduct:'Ruched Bust Sports',
                    price: 3900,
                    priceDiscount:2400
                }

            ] 
        }
    },
    methods: {
        hendleChecked : function(data) {
            this.isCondition =true;
            this.checked=data;
        },
        percentage : function(price,priceDis) {
            const total = Math.floor((priceDis-price) /price * 100);

            return total;
        }
    }
}
</script>
<style scoped lang="scss">

    @media only screen and (max-width: 46.1875em) {

        .container_content-right  {
            .icon_show-product .show__product-review {
                z-index: 1000;
                position:fixed !important;
                display: none;
                width: 260px;
                height: 420px;
                background-color: #fff;
                bottom: 0px;   
                top: 50%;
                transform: translate(50%,-50%);
                right: 50%; 
                z-index: 10px;


                .sale-product-imgs {
                    height:auto;
                    max-height: 455px;

                    .discount_product {
                        width:50px;
                    }
                }
            }
            .icon_show-product .show__product-review::after {
                display: none;
            }
        }
       
    }


    .icon_show-product:nth-child(1){
        top:100% !important;
        left:20% !important;
    }
    .icon_show-product:nth-child(2){
        top:40% !important;
        left:40% !important;
    }
    .icon_show-product:nth-child(3){
        top:70% !important;
        left:50% !important;
    }
    .icon_show-product:nth-child(4){
        top:35% !important;
        left:65% !important;
    }

    .container3 {
        width: 100%;
        height: 582px;
        background-image: url(https://cdn.shopify.com/s/files/1/0326/6517/4152/files/lookbook-background-fixed_1728x.png?v=1623912239);
        background-repeat: no-repeat;
        background-size:cover;
        display: flex;
        align-items: center;
    }
    .moldal {
    position: fixed;
    top:0;
    left:0;
    right:0;
    bottom:0;
    z-index: 1;
    }
    .ShowReview {
        position: absolute;
        width: 100%;
        height:100vh;
    }
    .container_content-left {

        .content-animated {
            margin-top: 160px;
            margin-left: 50px;
        }
         .animate_title-time {
            font-weight: 400;
            color: $title-text-color;
            font-size: 18px;
            font-family: $Inter;
            letter-spacing: .5px;
         }
         .animate__title {
            font-weight: 700;
            color: $title-text-color;
            font-size: 45px;
            letter-spacing: .5px;
            font-family: Poppins;
         }

        .animate_text {
            line-height: 25px;
            font-size: 14px;
            font-weight: 400;
            color: $title-text-color;
            margin-bottom: 10px;
             max-width: 60%;

         }
            
    }


    .btn-link {
        font-family: 'Inter', sans-serif;
        text-decoration: none;
        text-transform: uppercase;
        display: inline-flex;
        -ms-flex-align: center;
        align-items: center;
        -ms-flex-pack: center;
        justify-content: center;
        margin-bottom: 5px;
        border-radius: 0px;
        font-weight: 400;
        min-height: 40px;
        max-width: 200px;
        font-size: 13px;
        color: #ffffff;
        cursor: pointer;
        border: 2px solid #222;
        padding: 5px 30px;
        background-color: #000000;
        border-color: #000000;
        z-index: 10;

        &:hover span{
            transform: translateX(50%);
            @include transisons(transform,.4s);
        }

        span {
            transform: translateX(0);
            @include transisons(transform,.4s);
            font-size: 16px;
            margin-left: 5px;
        }       
    }
    .container_content-right {
        width: 100%;
        height: auto;
        display: flex;
        justify-content: center;
        position: relative;


        .icon_show-product {
            position: absolute;
            width:30px;
            height: 30px;
            left:20%;
            line-height:32px;
            text-align: center;
            border-radius: 50%;
            top: 50%;
            background-color:$color-h;
            color:#fff;
            @include  animations(zoompin,2s);
            cursor: pointer;
        }

        .icon_show-product.s-1 {
            position: absolute;
            top: 40% ;
            left: 40%;
        }

        .icon_show-product.s-2 {
            position: absolute;
            top: 30% ;
            left:70%;
        }

        .icon_show-product.s-3 {
            position: absolute;
            top: 60% ;
            left:50%;
        }

        .show__product-review {
            display: none;
            position: absolute;
            width:260px;
            height: 425px;
            background-color:#fff ;
            bottom:0px ;
           right:50px;
           z-index: 10px;

           &::after {
               content: "";
               bottom: 4px;
               right: -20px;
               position: absolute;
               border-left: 10px solid #fff ;
                border-right: 10px solid  transparent ;
                border-bottom: 10px solid transparent;
                border-top: 10px solid  transparent;
                display: inline-block;
                
           }
        }

        .show__product-review.active {
            display: block;
        }

      
    }

    .animate-picter {
        max-width: 765px;
        max-height: 455px;
        img {
            width: 100%;
            height:450px;
            object-fit: cover;
        } 
    }

    .show__product-review {
        align-items: center;
        box-shadow: 0 0 3px 1px rgb(153, 148, 148);
        z-index: 10 ;
        .sale-product-imgs {
            margin:5%;
            width: 90%;
            height: 350px;
        }
        .sale_product-link {
            text-align: center;
        }
        .sale_product-price {
            margin-left: 50px ;
        }
    }


   
</style>