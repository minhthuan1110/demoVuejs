<template>
    <div class="nav_title-sibar ">
        <div class="tags-title row">
            <div class="tags-title-left c-6 " :class="{active:isActiveMenu}" @click="isActiveMenu= true" >
                <span class="tags-text" v-on:click=" isShowCategoris=false">Menu</span>
            </div>
            <div class="tags-title-right c-6" :class="{active:isShowCategoris}" @click="isShowCategoris= true"  >
                <span class="tags-text" v-on:click=" isActiveMenu=false">CATEGORIES</span>
            </div>
        </div>
        <div class="tags-content1" :class="{active:isActiveMenu}">
            <ul class="list-Item-sibar">
                <DemoNav/>
                <ProducNav/>
                <SaleNav/>
                <ShopNav/>
                <BlogNav/>
                <LookbookNav/>
                <Sidebar/>
                <li class="list_nabar">
                    <i  class="far fa-heart i"></i>
                    <a href="" class="nav_link a">Wishlist</a>
                </li>
                <li class="list_nabar">
                    <i class="lab la-sistrix  icom_h i"></i>
                    <a href="" class="nav_link a">Search</a>
                </li>
                <li class="list_nabar">
                    <i class="las la-user-tie  icom_h i"></i>
                    <a href="" class="nav_link a">Login / Register</a>
                </li>
            </ul>
        </div>
        <div class="tags-content2" :class="{active:isShowCategoris}">
            <ul class="list-Item-sibar">
                <li class="list_nabar">
                    <i class="fas fa-female i"></i>
                    <a href="" class="nav_link a">Women’s Clothing</a>
                </li>
                <li class="list_nabar">
                    <i class="fas fa-male i"></i>
                    <a href="" class="nav_link a">Men’s Clothing</a>
                </li>
                <li class="list_nabar">
                    <i class="las la-user-tie  icom_h i"></i>
                    <a href="" class="nav_link a">Watches</a>
                </li>
                <li class="list_nabar">
                    <i class="las la-user-tie  icom_h i"></i>
                    <a href="" class="nav_link a">Acessories</a>
                </li>
                <li class="list_nabar">
                    <i class="las la-user-tie  icom_h i"></i>
                    <a href="" class="nav_link a">Electric</a>
                </li>
                <li class="list_nabar">
                    <i class="las la-user-tie  icom_h i"></i>
                    <a href="" class="nav_link a">Shoes</a>
                </li>
                <li class="list_nabar">
                    <i class="las la-user-tie  icom_h i"></i>
                    <a href="" class="nav_link a">T-Shirt</a>
                </li>
                <li class="list_nabar">
                    <i class="las la-user-tie  icom_h i"></i>
                    <a href="" class="nav_link a">Toys, Kids & Baby</a>
                </li>
                <li class="list_nabar">
                    <i class="las la-user-tie  icom_h i"></i>
                    <a href="" class="nav_link a">Decor</a>
                </li>
            </ul>
        </div>
    </div>
</template>

<script>
    import  DemoNav from '../navbar-left/DemoNav.vue';
    import  BlogNav from '../navbar-left/BlogNav.vue';
    import  LookbookNav from '../navbar-left/LookbookNav.vue';
    import  ProducNav from '../navbar-left/ProducNav.vue';
    import  SaleNav from '../navbar-left/SaleNav.vue';
    import  ShopNav from '../navbar-left/ShopNav.vue';
    import  Sidebar from '../sidebar/Sidebar.vue'

export default {
     components: {
        DemoNav,
        BlogNav,
        LookbookNav,
        ProducNav,
        SaleNav,
        ShopNav,
        Sidebar

    },
    data () {
        return {
            isActiveMenu:true,
            isShowCategoris:false,  
        }
    }
    
}
</script>

<style scoped lang="scss">
.tags-title {
    width: 100%;
    height:auto;
    margin:0;
    border-top: 1px solid rgba(129,129,129,.2);
    background-color: rgba(0,0,0,.04);
    border-bottom: 1px solid rgba(129,129,129,.2);

    .tags-title-left,
    .tags-title-right{
        text-align: center;
        text-transform: uppercase;
        letter-spacing: .3px;
        font-weight: 500;
        font-size: 12px;
        color: #222;
        padding: 5px 10px;
        line-height:40px;
        height: 55px;
        -ms-flex: 0 0 100%;
        flex: 0 0 100%;
        // max-width: 100%;
        cursor: pointer;
        font-family:$Inter ;

        .tags-text {
            display: block;
            width: 100%;
            height: 100%;
        }
    }
    .tags-title-left.active,
    .tags-title-right.active{
        background-color: rgba(0,0,0,.05);
        border-bottom: 2px solid $color-h;

    }

    
}
.tags-content1, .tags-content2 {
        display:none;   
    }
    .tags-content1.active {
        display: block;
        width: 100%;
        height: auto;

    }

    .tags-content2.active {
        display: block;
        width: 100%;
        height: auto;
    }
</style>