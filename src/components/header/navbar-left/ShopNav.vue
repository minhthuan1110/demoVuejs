<template>
    <li class="list_nabar" @click="isShowListLink = !isShowListLink">
        <a href="" class="nav_link" :class="{active:isShowListLink}">shop
            <div class="list_show-icon">
                <div class="hendle-icon" :class="{active:isShowListLink}">
                <span class="hendle__icon-add">
                    <i class="fas fa-plus"></i>
                </span>
                <span class="hendle__icon-close">
                    <i class="fas fa-minus"></i>
                </span>  
                </div>
                <i class="fas fa-check"></i>
            </div>
        </a>
      <div class="nav_showlist row" :class="{active:isShowListLink}">
          <div class="nav_item l-4">
              <div class="row">
                  <div class="nav_item l-6">
                      <h5 class="navbar_item-title">
                          HOMEPAGES
                      </h5>
                      <ul class="nav_item-content">
                          <li class="navbar_item-list">
                              <a href="" class="navbar_item-link">
                                  Home Default
                                  <span class="navbar_item-new" > hot</span>
                              </a>
                          </li>
                          <li class="navbar_item-list">
                              <a href="" class="navbar_item-link">
                                  Home Default
                                  <span class="navbar_item-hot" >new</span>
                              </a>
                          </li>
                          <li class="navbar_item-list">
                              <a href="" class="navbar_item-link">
                                  Home Default
                                  <span class="navbar_item-hot" >new</span>
                              </a>
                          </li>                                     
                      </ul>
                  </div>
                  <div class="nav_item l-6">
                      <h5 class="navbar_item-title">
                          HOMEPAGES
                      </h5>
                      <ul class="nav_item-content">
                          <li class="navbar_item-list">
                              <a href="" class="navbar_item-link">
                                  Home Default
                                  <span class="navbar_item-new" > hot</span>
                              </a>
                          </li>
                          <li class="navbar_item-list">
                              <a href="" class="navbar_item-link">
                                  Home Default
                                  <span class="navbar_item-hot" >new</span>
                              </a>
                          </li>
                          <li class="navbar_item-list">
                              <a href="" class="navbar_item-link">
                                  Home Default
                                  <span class="navbar_item-hot" >new</span>
                              </a>
                          </li>                                     
                      </ul>
                  </div>
              </div>
          </div>
          <div class="nav_item l-8">
              <div class="nav-show__item row ">
                  <div class="item__product col l-6">
                      <a href="" class="item__product-link">
                          <div class="item__product-img-left"></div>
                          <div class="btn_product">
                              <span class="btn_product-text">Women’s Outfit</span>
                          </div>
                      </a>
                  </div>
                  <div class="item__product col l-6">
                      <a href="" class="item__product-link">
                          <div class="item__product-img-right"></div>
                          <div class="btn_product">
                              <span class="btn_product-text">Women’s Outfit</span>
                          </div>
                      </a>
                  </div>
              </div>
          </div>
      </div>
  </li>
</template>

<script>

export default {
  data(){
      return {
          isShowListLink :false
      }
  }
}
</script>

<style>
   body {
    margin: 0;
    padding: 0;
  }
</style>
