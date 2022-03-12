<template>
    <div class="container4">
        <h2 class="contaner-title">new arrivals</h2>
        <span class="container_title-text">Quis nostrum exercitationem ullam corporis suscipit laboriosam, nisi ut aliquid.</span>
        <div class="container1-r  grid wide">
            <div class="container1-content product-show row ">
                <div class="container_content-product col l-4 m-6 c-12">
                    <div class="nacv-blog">
                        <a href="">
                            <img src="	https://cdn.shopify.com/s/files/1/0326/6517/4152/articles/blog-3_1296x.png?v=1623839549" alt="">
                        </a>
                    </div>
                    <span class="blog_logtime">
                        on <span>JUNE 16, 2021</span>
                    </span>
                    <h4 class="blog_title"><a href="">Getting Ready With: Rebecca</a> </h4>
                    <p class="blog_content">As the capability to create typography has become ubiquitous, the application of principles and best practices dev...</p>
                </div>
                <div class="container_content-product col l-4 m-6 c-0">
                    <div class="nacv-blog">
                        <a href="">
                            <img src="	https://cdn.shopify.com/s/files/1/0326/6517/4152/articles/blog-1_720x.png?v=1623839571" alt="">
                        </a>
                    </div>
                    <span class="blog_logtime">
                        on <span>JUNE 16, 2021</span>
                    </span>
                    <h4 class="blog_title"><a href="">Getting Ready With: Rebecca</a> </h4>
                    <p class="blog_content">As the capability to create typography has become ubiquitous, the application of principles and best practices dev...</p>
                </div>
                <div class="container_content-product col l-4 m-6 c-0">
                    <div class="nacv-blog">
                        <a href="">
                            <img src="https://cdn.shopify.com/s/files/1/0326/6517/4152/articles/blog-2_720x.png?v=1623839406" alt="">
                        </a>
                    </div>
                    <span class="blog_logtime">
                        on <span>JUNE 16, 2021</span>
                    </span>
                    <h4 class="blog_title"><a href="">Getting Ready With: Rebecca</a> </h4>
                    <p class="blog_content">As the capability to create typography has become ubiquitous, the application of principles and best practices dev...</p>
                </div>
            </div>
        </div>
    </div>
</template>
<script>
export default {
    
}
</script>

<style lang="scss" scoped>
    .container4 {
        margin-top:100px;
        width: 100%;
        text-align: center;
        
        .container1-content.product-show {
            justify-content:start;
        }
    }

    .container1-content.product-show {
        margin: 30px 0px;
    }

    .nacv-blog {
        width: 100%;
        max-height:292px;
        position: relative;

        img{ 
            width: 100%;
            max-height:292px;

        }

        &::after {
            content: "";
            position: absolute;
            top:50%;
            left:50%;
            transform: translate(-50%,-50%);
            width:5px;
            height:5px;
            border-radius: 50%;
            // box-shadow: 0 0 5px 2px rgba(223, 215, 215, 0.308);
            z-index: 1;
        }

    }

    .blog_logtime {
        width: 100%;
        line-height: 30px;
        font-family: $Inter;
        font-size:14px;
        color:$text-color;

        


        span { 
            font-size:13px;
            color:#000;
            font-weight:600;
            text-transform: uppercase;
        }
    }

    .blog_title {
        font-size: 16px;
        font-weight: 600;
        line-height: 1.428;
        font-family: Poppins;
        a { 
            text-decoration: none;
            color:$title-text-color;

            &:hover {
                color:$color-h;
            }
        }
        
    }

    .blog_content {
         font-family: $Inter;
         margin-top:5px ;
        font-size:14px;
        color:$text-color;
    }

    .container_content-product:hover .nacv-blog::after {
             animation-delay: .4s;
            @include animation(zoompins, .5s) ;
    }
</style>