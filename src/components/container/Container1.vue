<template>
    <div class="container1">
        <h2 class="contaner-title">shop by categories</h2>
        <span class="container_title-text">Quis nostrum exercitationem ullam corporis suscipit laboriosam, nisi ut aliquid.</span>
        <div class="container1-r grid wide">
            <div class="container1-content row">
                <div class="container_content-left l-6 m-12 c-12">
                    <div class="item__product col l-12">
                        <a href="" class="item__product-link">
                            <div class="item__product-img-left img1"></div>
                            <div class="btn_product">
                                <span class="btn_product-text">Women’s Outfit</span>
                            </div>
                        </a>
                    </div>

                </div>
                <div class="container_content-right l-6 m-12 c-12">
                    <div class="nav-show__item row ">
                        <div class="item__product col l-6 m-6 c-6">
                            <a href="" class="item__product-link center">
                                <div class="item__product-img-left img2"></div>
                                <div class="btn_product">
                                    <span class="btn_product-text">Women’s Outfit</span>
                                </div>
                            </a>
                            <a href="" class="item__product-link">
                                <div class="item__product-img-left img3"></div>
                                <div class="btn_product">
                                    <span class="btn_product-text">Women’s Outfit</span>
                                </div>
                            </a>
                        </div>
                        <div class="item__product col l-6 m-6 c-6">
                            <a href="" class="item__product-link right">
                                <div class="item__product-img-left img4"></div>
                                <div class="btn_product">
                                    <span class="btn_product-text">Women’s Outfit</span>
                                </div>
                            </a>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>
<script>
export default {
    
}
</script>
<style scoped lang="scss">
    .container1 .container1-r {
        margin-top:20px;
        width:100%;
        height:750px ;

        .container_content-left {
            width: 100%;
            height: 100%;
            .item__product-link {
                width: 100%;
                margin:0 -12px;
                height: 750px;
                &:hover .product-img-show-left {
                    transform: scale(1.1);
                }
            }
            .item__product-img-left.img1{
                background-image: url(https://cdn.shopify.com/s/files/1/0326/6517/4152/files/51_900x.jpg?v=1623835818);
            }
        }

        .container_content-right {
            width: 100%;
            height: 100%;
            .item__product-link {
                width: 105%;
                margin:0 -12px;
                height: 358px;
                &:hover .product-img-show-left {
                    transform: scale(1.1);
                }
            }

            .item__product-link.right {
                height: 750px;
            }
            .item__product-link.center {
                margin-bottom: 35px;
            }
            .item__product-img-left.img2{
                background-image: url(	https://cdn.shopify.com/s/files/1/0326/6517/4152/files/53877734_266_a_360x.png?v=1623836446);
            }
            .item__product-img-left.img3{
                background-image: url(https://cdn.shopify.com/s/files/1/0326/6517/4152/files/52_360x.jpg?v=1623835818);
            }
            .item__product-img-left.img4{
                background-image: url(	https://cdn.shopify.com/s/files/1/0326/6517/4152/files/51051126_023_0_360x.jpg?v=1623835818);
            }
        }
    }
</style>