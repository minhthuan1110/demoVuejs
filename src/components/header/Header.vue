<template>
<div class="header " >
    <div class="header-top grid">
        <div class="header__nav grid wide" >
            <div class="header__list-nav row no-gutters ">
                <div class="header__list-navitem-left  l-5">
                    <ul class="navbar row">
                    <DemoNav/>
                    <ShopNav/>
                    <ProducNav/>
                        <SaleNav/>
                        <LookbookNav/>
                        <BlogNav/>
                    </ul>
                </div>
                <div class="header_icon--navbar m-5 c-5 " v-on:click="isActive=true" >
                    <i class="las la-align-left" @click="isShow= !isShow"></i>
                </div>

                <div class="header__list-navitem col l-2 m-2 c-2">
                    <Baner/>
                </div>
                <div class="header__list-navitem-right col l-5 m-5 c-5">
                    <NabarRight />
                </div>
            </div>
            <div class="moldal--show" v-show="isShow">
                <div class="modal-show_sidebar" :class="{active:isActive}" >
                    <Sidebar/>
                </div>
                <div class="modal-close" :class="{active:isActive}" >
                        <i class="fas fa-times" @click="isShow= false"></i>
                </div>
                <div class="moldal" v-show="isShow" @click="isShow= !isShow">
                    
                </div>
            </div>
        </div>
    </div>
    
    <Slider/>
    <SeconsDown/>
</div>

</template>
<script>
import  DemoNav from './navbar-left/DemoNav.vue';
import  BlogNav from './navbar-left/BlogNav.vue';
import  LookbookNav from './navbar-left/LookbookNav.vue';
import  ProducNav from './navbar-left/ProducNav.vue';
import  SaleNav from './navbar-left/SaleNav.vue';
import  ShopNav from './navbar-left/ShopNav.vue';
import  Baner from './baner-img/Baner.vue';
import  NabarRight from './navbar-right/NabarRight.vue';
import  Sidebar from './sidebar/Sidebar.vue';
import  Slider from './slider/Slider'
import  SeconsDown from './secons-down/SeconsDown.vue';


export default {
    components: {
        DemoNav,
        BlogNav,
        LookbookNav,
        ProducNav,
        SaleNav,
        ShopNav,
        Baner,
        NabarRight,
        Sidebar,
        Slider,
        SeconsDown 

    },
    data () {
        return {
            isActive:false,
            isShow:false,  
        }
    },
    created () {
        window.addEventListener('scroll', this.handleScroll);
    },
    destroyed () {
        window.removeEventListener('scroll', this.handleScroll);
    },
    methods: {
        handleScroll () {
        let addClass = document.querySelector('.header .header-top' );

        if (window.scrollY > 100) {
            addClass.classList.add("active");
        }
        else { 
            addClass.classList.remove("active");
        }
        }
    }
    
}
</script>
<style lang='scss' >
    .header {
        width: 100%;
        height:auto;

        .header-top {
            width: 100%;
            height:auto;

            .header__nav {
                width: auto;
                height:auto;
                
            }

            
        }
        .header-top.active{
            position: fixed;
            top: 0;
            left: 0;
            right: 0;
            z-index: 1001;
            background-color:#fff;
            transition: all .6s;    
                
        }
    }

    .header__list-nav-left {
        position: relative;

        .header__list-navitem {
            width:100%;
        }
    }

    .header__list-navitem-right {
         display: flex;
         flex-direction: row-reverse;

        .header__list-navitem {
            width:100%;

             
        }
        .navbar {

            .list_nabar {
                 line-height: 70px;
                 transform: translateY(5px);

                 .nav_icon-link {
                     width:100%;
                     height:100%;
                     color: $title-text-color;
                     @include transison;

                     &:hover{
                        color: $color-h;
                    }

                 }
             }
        }

    }

    .nav_icon-link {
            position: relative;
            span{
                position: absolute;
                width: 15px;
                height: 15px;
                border-radius: 50%;
                background-color:$title-text-color;
                top: -12px;
                right: 0;
                color: $white-color;
                line-height: 15px;
                text-align: center;
                font-size: 10px;
            }
        
    }

    .navbar {
        list-style: none;
        margin:0 11px;
        height:70px;
        
        .list_nabar {
            line-height: 70px;

            &:hover .nav_showlist {
                display:flex;
            }

            &:hover .nav_link{
                color: $color-h;
                cursor: pointer; 
            }
            &:hover .nav_showlist{
                @include animation(gowup,.4s);
            }
        }
    }

    .nav_link {
        width:100%;
        height:100%;
        text-decoration: none;
        padding: 0 17px;
        font-weight: 500;
        font-size: 14px;
        font-family: $Inter;
        text-transform: uppercase;
        color: $title-text-color;
        position: relative;
        @include transison;

        i {
            color: rgba(82,82,82,.45);
            font-size:8px ;
            top:22%;
            padding-left: 5px;
            position:absolute;
            
        }
    }


    .nav_icon-link {
        width:100%;
        height:100%;
        text-decoration: none;
        font-weight: 500;
        padding: 0 8px;
        font-size: 14px;
        font-family: $Inter;
        text-transform: uppercase;
        color: $title-text-color;
        position: relative;
        padding: 0 -7px;
        .icom_h {
            font-size: 28px;
            -webkit-font-smoothing: antialiased;
            display: inline-block;
            font-style: normal;
            font-variant: normal;
            text-rendering: auto;
        }
    }

    .header__list-navitem {
        width: auto;
        height: auto;
        display:flex;
        align-items: center;

        .heder__img-link {
            text-decoration: none;
            width: 107%;
            height:30px;

            .header_item-img{
                width:inherit;
                height:inherit;	
            }
        }

    }
    .list_nabar {
        position: relative;
        .nav_showlist {
            margin: 0 15px;
            top: 70px;
            left:0;
            max-height: 550px;
            width:1150px;
            position: absolute;
            background-color:$white-color;
            overflow-y: auto;
            box-shadow: inset 0 0 0 1px #eaeaea, 0 5px 20px rgb(0 0 0 / 15%);
            z-index: 100;
        }
    }
    .nav_showlist {
        display: none;
            .nav_item {
                padding: 30px 20px;
                
                .navbar_item-title {
                    color:$title-text-color;
                    text-transform: uppercase;
                    font-weight: 500;
                    font-size: 12px;
                    padding: 13px 0;
                    border-bottom: 1px solid #eee;
                    line-height: 12px;
                    font-family: $Inter;
                    font-weight: 500;
                }

            }
        }
    
    .nav_item-content {
        .navbar_item-list{
            font-size: 14px;
            list-style: none;
            position: relative;
            font-family: $Inter;

            .navbar_item-link {
                text-decoration: none;
                padding: 10px 0;
                display: block ;
                color: $text-color;
                position: relative;
                line-height: 1.5;
                 @include transison;
                &:hover {
                    color: $title-text-color;
                }
            
                .navbar_item-hot {
                    position: absolute;
                    width: 30px;
                    height: 15px;
                    
                    background: #01bad4;
                    color: #fff;
                    border-radius: 10px;
                    text-align: center;
                    font-size: 10px;
                    line-height: 15px;
                    margin: 0 5px;
                }

                .navbar_item-new {
                    position: absolute;
                    width: 30px;
                    height: 15px;
                    color: #fff;
                    line-height: 15px;
                    background-color: #ff3e11;                 
                    border-radius: 10px;
                    text-align: center;
                    font-size: 10px;
                    margin: 0 5px;
                }
            }
        }

    }


    .nav-show__item {
        width: 100%;
        height:auto;

        .item__product {
        //    padding-left:15px;
        //    padding-right:15px;

        }
    }

    .item__product-link {
        display: block;
        width: 92%;
        height: 435px;
        position: relative;
        overflow: hidden;
        backface-visibility: hidden;
        -webkit-backface-visibility: hidden;
        

        .item__product-img-left {
            background-image: url(https://cdn.shopify.com/s/files/1/0326/6517/4152/files/58421298_045_d_360x.jpg?v=1623909979);
            animation: 1.25s cubic-bezier(.26,.54,.32,1) forwards ani-fadeIn;
            display: block;
            width: 100%;
            height: 100%;
            position: relative;
            background-repeat: no-repeat;
            background-size: cover;
            @include transisons(transform,.7s);
            background-position: center center;

            &:hover {
                transform:scale(1.1);
            }
        }
        .item__product-img-right {
            background-image: url(https://cdn.shopify.com/s/files/1/0326/6517/4152/files/58421298_001_c_360x.jpg?v=1623909979);
            animation: 1.25s cubic-bezier(.26,.54,.32,1) forwards ani-fadeIn;
            display: block;
            width: 100%;
            height: 100%;
            position: relative;
            background-repeat: no-repeat;
            background-size: cover;
            @include transisons(transform,.7s);
            background-position: center center;

            &:hover {
                transform:scale(1.1);
            }
        }
        

    }
    .header_icon--navbar {
    width: 100%;
    height:70px;
    i {
        font-size: 35px;
        line-height:70px;
        margin: 0 15px;
        cursor: pointer;
    }
   }

.modal-show_sidebar.active {
    @include animation(gowleft,.6s);
    left:0;
}


.modal-close {
    position: absolute;
    display: block;
    right: 0%;
    z-index: 5;
    width: 30px;
    text-align: center;
    color:rgb(197, 177, 177);
    font-size: 30px;
    background-color: rgb(15, 15, 15);
    font-style: normal;
    font-weight: 400;
    font-variant: normal;
    text-transform: none;
    line-height: 1;
   

}
.modal-close.active {
    @include animation(gowright,.6s);
    right: 20%;
    transform:translateX(100%);
}

</style>