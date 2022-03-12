<template>
    <div>
         <div class="footer grid">
            <div class="footer__nav grid wide">
                <div class="footer__list-nav row no-gutters ">
                    <div class="footer__list-navitem col l-3 m-6 c-12">

                        <div class="show-footer footer__newsletter row" @click ="isShowTouch=!isShowTouch" >
                            <h4 class=" footer__newsletter-title">Get in touch</h4>
                            <div class="hendle-icon " :class="{active:isShowTouch}">
                                <span class="hendle__icon-add">
                                    <i class="fas fa-plus"></i>
                                </span>
                                <span class="hendle__icon-close">
                                    <i class="fas fa-minus"></i>
                                </span>
                            </div>
                        </div>
                       <div class="shownews-letter"  :class="{active:isShowTouch}">
                             <a class="heder__img-link"  href="">
                                 <img src="https://cdn.shopify.com/s/files/1/0326/6517/4152/files/Kalles_demo.svg?v=12375657845510483766" alt="" class="header_item-img">
                            </a>
                            <ul class="list-Item-footer">
                                <li class="list_nabar">
                                    <i class="las la-map-marker-alt"></i>
                                    <span>184 Main Rd E, St Albans <br> VIC 3021, Australia</span>
                                </li>
                                <li class="list_nabar">
                                    <i class="las la-envelope"></i>
                                    <a href="" class="link__email">contact@company.com</a>
                                </li>
                                <li class="list_nabar">
                                    <i class="las la-phone"></i>
                                    <span>+001 2233 456</span>
                                </li>
                            </ul>
                            <div class="footer__infor row">
                                <div class="footer__infor-list">
                                    <a href="" class="footer__infor-link">
                                        <i class="lab la-facebook-f"></i>
                                    </a>
                                
                                </div>
                                <div class="footer__infor-list">
                                    <a href="" class="footer__infor-link">
                                        <i class="lab la-twitter"></i>
                                    </a>
                                    
                                </div>
                                <div class="footer__infor-list">
                                    <a href="" class="footer__infor-link">
                                        <i class="lab la-instagram"></i>
                                    </a>
                                    
                                </div>
                                <div class="footer__infor-list">
                                    <a href="" class="footer__infor-link">
                                        <i class="fab fa-linkedin-in"></i>
                                    </a>           
                                </div>
                                <div class="footer__infor-list">
                                    <a href="" class="footer__infor-link">
                                        <i class="fab fa-pinterest-p"></i>
                                    </a>           
                                </div>
                            </div>
                       </div>
                    </div>
                    <div class="footer__list-navitem col l-6 m-12 c-12">
                        <div class="nav_showlist row">
                            <div class="nav_item l-4 m-4 c-12">      
                                <div class="show-footer row" @click ="isShowCategoris=!isShowCategoris" >
                                    <h5 class="navbar_item-title">
                                        Categories
                                    </h5>
                                    <div class="hendle-icon " :class="{active:isShowCategoris}">
                                        <span class="hendle__icon-add">
                                            <i class="fas fa-plus"></i>
                                        </span>
                                        <span class="hendle__icon-close">
                                            <i class="fas fa-minus"></i>
                                        </span>
                                    </div>
                                </div>
                                <ul class="nav_item-content  " :class="{active:isShowCategoris}">
                                    <li class="navbar_item-list">
                                        <a href="" class="navbar_item-link">
                                            Women
                                        </a>
                                    </li>
                                    <li class="navbar_item-list">
                                        <a href="" class="navbar_item-link">
                                            Accessories
                                        </a>
                                    </li>
                                    <li class="navbar_item-list">
                                        <a href="" class="navbar_item-link">
                                            Footwear
                                        </a>
                                    </li>
                                    <li class="navbar_item-list">
                                        <a href="" class="navbar_item-link">
                                            Men’s Outfit
                                        </a>
                                    </li>
                                    <li class="navbar_item-list">
                                        <a href="" class="navbar_item-link">
                                            Sweatpants
                                        </a>
                                    </li>
                                    <li class="navbar_item-list">
                                        <a href="" class="navbar_item-link">
                                            Women’s Outfit
                                            <span class="navbar_item-hot" >new</span>
                                        </a>
                                    </li>
                                                                    
                                </ul>
                            </div>
                            <div class="nav_item l-4 m-4 c-12">
                                <div class="show-footer row" @click ="isShowInformation=!isShowInformation" >
                                    <h5 class="navbar_item-title">
                                        Information
                                    </h5>
                                    <div class="hendle-icon " :class="{active:isShowInformation}">
                                        <span class="hendle__icon-add">
                                            <i class="fas fa-plus"></i>
                                        </span>
                                        <span class="hendle__icon-close">
                                            <i class="fas fa-minus"></i>
                                        </span>
                                    </div>
                                </div>
                                <ul class="nav_item-content" :class="{active:isShowInformation}">
                                    <li class="navbar_item-list">
                                        <a href="" class="navbar_item-link">
                                            About Us
                                        </a>
                                    </li>
                                    <li class="navbar_item-list">
                                        <a href="" class="navbar_item-link">
                                            Contact Us
                                        </a>
                                    </li>
                                    <li class="navbar_item-list">
                                        <a href="" class="navbar_item-link">
                                            Terms & Conditions
                                        </a>
                                    </li>
                                    <li class="navbar_item-list">
                                        <a href="" class="navbar_item-link">
                                            Returns & Exchanges
                                        </a>
                                    </li> 
                                    <li class="navbar_item-list">
                                        <a href="" class="navbar_item-link">
                                            Shipping & Delivery
                                        </a>
                                    </li>
                                    <li class="navbar_item-list">
                                        <a href="" class="navbar_item-link">
                                            Privacy Policy
                                        </a>
                                    </li>                                    
                                </ul>
                            </div>
                            <div class="nav_item l-4 m-4 c-12">
                                <div class="show-footer row" @click ="isShowQuickLinks=!isShowQuickLinks" >
                                    <h5 class="navbar_item-title">
                                        Quick Links
                                    </h5>
                                    <div class="hendle-icon " :class="{active:isShowQuickLinks}">
                                        <span class="hendle__icon-add">
                                            <i class="fas fa-plus"></i>
                                        </span>
                                        <span class="hendle__icon-close">
                                            <i class="fas fa-minus"></i>
                                        </span>
                                    </div>
                                </div>
                                <ul class="nav_item-content" :class="{active:isShowQuickLinks}">
                                    <li class="navbar_item-list">
                                        <a href="" class="navbar_item-link">
                                            Store Location
                                        </a>
                                    </li>
                                    <li class="navbar_item-list">
                                        <a href="" class="navbar_item-link">
                                            My Account
                                        </a>
                                    </li>
                                    <li class="navbar_item-list">
                                        <a href="" class="navbar_item-link">
                                            Latest News
                                        </a>
                                    </li>
                                    <li class="navbar_item-list">
                                        <a href="" class="navbar_item-link">
                                            Size Guide
                                        </a>
                                    </li> 
                                    <li class="navbar_item-list">
                                        <a href="" class="navbar_item-link">
                                            FAQs
                                        </a>
                                    </li>
                                    <li class="navbar_item-list">
                                        <a href="" class="navbar_item-link">
                                            Privacy Policy
                                        </a>
                                    </li>                                    
                                </ul>
                            </div>
                        </div>
                    </div>
                    <div class="footer__list-navitem col l-3 m-6 c-12">
                        <div class="footer__newsletter">
                            <div class="show-footer row" @click ="isShowNewsletter=!isShowNewsletter" >
                                <h4 class=" footer__newsletter-title mb">Newsletter Signup</h4>
                                <div class="hendle-icon " :class="{active:isShowNewsletter}">
                                    <span class="hendle__icon-add">
                                        <i class="fas fa-plus"></i>
                                    </span>
                                    <span class="hendle__icon-close">
                                        <i class="fas fa-minus"></i>
                                    </span>
                                </div>
                            </div>
                            <div class="shownews-letter" :class="{active:isShowNewsletter}">
                                <p class="footer__newsletter-text">Subscribe to our newsletter and get 10% off your first purchase</p>
                                <div class="send_emial">
                                    <input type="text" class="send_emial-text" placeholder="your mail address">
                                    <button type="submit" class="btn-submit">Subcribe</button>
                                </div>
                                <div class="footer__infor row">
                                    <div class="footer__infor-list">
                                    <img src="https://cdn.shopify.com/shopifycloud/shopify/assets/payment_icons/amazon-92e856f82cae5a564cd0f70457f11af4d58fa037cf6e5ab7adf76f6fd3b9cafe.svg" alt="" class="footer__logos">
                                    </div>
                                    <div class="footer__infor-list">
                                        <img src="https://cdn.shopify.com/shopifycloud/shopify/assets/payment_icons/american_express-2264c9b8b57b23b0b0831827e90cd7bcda2836adc42a912ebedf545dead35b20.svg" alt="" class="footer__logos">     
                                    </div>
                                    <div class="footer__infor-list">
                                        <img src="https://cdn.shopify.com/shopifycloud/shopify/assets/payment_icons/apple_pay-f6db0077dc7c325b436ecbdcf254239100b35b70b1663bc7523d7c424901fa09.svg" alt="" class="footer__logos">    
                                    </div>
                                    <div class="footer__infor-list">
                                        <img src="https://cdn.shopify.com/shopifycloud/shopify/assets/payment_icons/bitcoin-e41278677541fc32b8d2e7fa41e61aaab2935151a6048a1d8d341162f5b93a0a.svg    " alt="" class="footer__logos">
                                    </div>
                                    <div class="footer__infor-list">
                                        <img src="https://cdn.shopify.com/shopifycloud/shopify/assets/payment_icons/discover-cc9808e50193c7496e7a5245eb86d5e06f02e2476c0fe70f2c40016707d35461.svg" alt="" class="footer__logos">
                                    </div>
                                    <div class="footer__infor-list">
                                        <img src="https://cdn.shopify.com/shopifycloud/shopify/assets/payment_icons/dogecoin-40c07eb6559d1c47a2ac893d14a4d27cdfad770df3413fb3e49ab51a18c8961d.svg" alt="" class="footer__logos">
                                    </div>
                                    <div class="footer__infor-list">
                                        <img src="https://cdn.shopify.com/shopifycloud/shopify/assets/payment_icons/google_pay-c66a29c63facf2053bf69352982c958e9675cabea4f2f7ccec08d169d1856b31.svg" alt="" class="footer__logos">
                                    </div>
                                    <div class="footer__infor-list">
                                        <img src="https://cdn.shopify.com/shopifycloud/shopify/assets/payment_icons/jcb-ab0f5a1739704f1ab039f19ac8c28895af5c39a3f54ee9b748ea051986b0bd36.svg" alt="" class="footer__logos">
                                    </div>
                                    <div class="footer__infor-list">
                                        <img src="https://cdn.shopify.com/shopifycloud/shopify/assets/payment_icons/maestro-d2055c6b416c46cf134f393e1df6e0ba31722b623870f954afd392092207889c.svg" alt="" class="footer__logos">
                                    </div>
                                    <div class="footer__infor-list">
                                        <img src="https://cdn.shopify.com/shopifycloud/shopify/assets/payment_icons/paypal-49e4c1e03244b6d2de0d270ca0d22dd15da6e92cc7266e93eb43762df5aa355d.svg" alt="" class="footer__logos">
                                    </div>
                                    <div class="footer__infor-list">
                                        <img src="https://cdn.shopify.com/shopifycloud/shopify/assets/payment_icons/shopify_pay-100fde795157a3d1c18042346cf8dbd1fcf4c4f53c20064e13ea2799eb726655.svg" alt="" class="footer__logos">
                                    </div>
                                    <div class="footer__infor-list">
                                        <img src="https://cdn.shopify.com/shopifycloud/shopify/assets/payment_icons/visa-319d545c6fd255c9aad5eeaad21fd6f7f7b4fdbdb1a35ce83b89cca12a187f00.svg" alt="" class="footer__logos">
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>

        <div class="footer-end grid">
            <div class="footer-end__nav grid wide">
                <div class="footer-end__list-nav row no-gutters ">
                    <div class="footer-end-text">
                        <span> Copyright © 2022 <span class="red"> Kalles</span>   All Rights Reserved. Powered by The4</span>
                    </div>
                    <div class="footer-end-text">
                        <ul class="footer__list row">
                            <li class="footer__list-nav">
                                <a href="">Shop</a>
                            </li>
                            <li class="footer__list-nav">
                                <a href="">About Us</a>
                            </li>
                            <li class="footer__list-nav">
                                <a href="">Contact</a>
                            </li>
                            <li class="footer__list-nav">
                                <a href="">Blog</a>
                            </li>
                        </ul>
                    </div>
                </div>
            </div>
        </div>           
    </div>
</template>
<script>
export default {
    data () {
        return { 
            isShowCategoris: false,
            isShowInformation:false,
            isShowQuickLinks:false,
            isShowTouch:false,
            isShowNewsletter:false,

        }
    }
}
</script>
<style scoped lang="scss">
    
    .footer-end {
        background-color: #ffffff;
        width: 100%;
        max-height:60px;
        .footer-end__nav {
            .footer-end__list-nav {
                justify-content:space-between;
                margin:0 20px;
                line-height: 60px;
                color: #696969;
                font-family: $Inter;
                font-size: 14px;
                .red {
                    color: $color-h;
                }
            }
            .footer__list {
                list-style: none;
                padding: 0 20px;
                .footer__list-nav {
                    margin-right:20px ;

                    a {
                        text-decoration: none;
                        color: #696969;
                        font-family: $Inter;
                        font-size: 14px;

                        &:hover {
                            color: $color-h;
                        }
                    }
                }
               
            }
        }
    }

    .footer {
        background-color: #ffead6;
    }

    .footer__nav {
        padding: 80px 0 30px 0;

        .footer__list-nav {
            width: 100%;
            padding-right: 15px;
            padding-left: 15px;
        }
    }
    

    .heder__img-link {
        text-decoration: none;
        outline: 0 ;

        .header_item-img {
            max-width: 105px;
            height: auto;
            vertical-align: middle;
            margin-bottom: 30px;
        }
    }
    .list-Item-footer {
        width : 100%;
        .list_nabar {
            list-style: none;
            margin-bottom: 15px;
            color: #000;
            font-size: 24px;
            margin-right: 5px;
            vertical-align: middle;
            font-weight: 400;
            font-variant: normal;
            text-transform: none;
            line-height: 1; 
        
            span {
                color: #696969;
                font-size:14px;
                line-height: 1.4;
                line-height: 24px;
                font-family: $Inter;
                margin-left: 10px;
            }

            .link__email {
                text-decoration: none;
                color: #696969;
                font-size:14px;
                line-height: 1.4;
                line-height: 24px;
                font-family: $Inter;
                margin-left: 10px;

                &:hover {
                    color: $color-h;
                }

            }
        }
    }
    .footer__infor {
        margin: 0;    
        .footer__infor-list {
            margin-right: 20px;
            margin-top: 0;
            @include transisons(margin-top,.4s);
            .footer__infor-link {
                text-decoration: none;
                color: #696969;        
            }

            &:hover{
                margin-top:-5px !important;
                @include transisons(margin-top,.4s); 
            }
            &:hover i{
                color: #56cfe1;
            }       
        }
    }
    .footer__list-navitem {
        .nav_showlist {
            .nav_item {
                padding: 0;

                .navbar_item-title {
                    font-size: 17px;
                    font-weight:600;
                    font-family: $Inter;
                    text-transform:capitalize;
                    margin-bottom: 15px;

                    
                }

                .nav_item-content {
                    .navbar_item-link {
                        padding: 5px 0;
                        &:hover {
                            color: $color-h;
                        }
                    }
                }
            }
        }

        .footer__newsletter {
            margin: 7px 0;
            .footer__newsletter-title {
                font-size: 17px;
                font-weight: 600;
                font-family: "Inter", sans-serif;
                text-transform: capitalize;
                margin-bottom: 30px;
            }

            .footer__newsletter-text {
                color: #696969;
                font-size: 14px;
                line-height: 1.4;
                line-height: 24px;
                font-family: "Inter", sans-serif;
                margin-bottom: 18px;
            }

            .send_emial {

                .send_emial-text {
                    outline:none;
                    border: 1px solid #878787;
                    padding: 0 10px;
                    font-size: 13px;
                    height: 40px;
                    line-height: 18px;
                    transition: border-color .5s;
                    box-shadow: none;
                    background-color: transparent;
                }

                .btn-submit {
                    color: #ffffff;
                    background-color: #000000;
                    appearance: none;
                    text-transform: none;
                    height: 41px;
                    max-width: 38%;
                    font-size: 14px;
                    padding: 0 20px;
                    border: none;
                    background: #222;
                    color: #fff;
                }
            }
            .footer__infor {
                margin: 20px 0 ;

                .footer__infor-list {
                    margin-right: 5px;

                    .footer__logos {
                        padding: 2.5px;
                        height: 34px;
                    }
                }

            }
        }
    }
</style>