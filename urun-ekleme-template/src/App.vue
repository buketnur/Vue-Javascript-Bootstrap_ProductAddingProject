<template>
<div>
  <app-navbar></app-navbar>
  <div class="container">
    <h1 class="text-center text-purple">Yeni Ürün Ekle</h1>
    <hr>
    <app-new-product></app-new-product>
    <br><br>
    <app-progress></app-progress>
    <br><br>
    
    <app-products></app-products>

  </div>
</div>
</template>

<script>
import NewProduct from "./components/NewProduct";
import AppProgress from "./components/AppProgress.vue";
import AppProducts from "./components/AppProducts.vue";
import AppNavbar from "./components/AppNavbar.vue";

export default {
  components: {
    appNavbar: AppNavbar,
    appNewProduct: NewProduct,
    appProgress: AppProgress,
    appProducts: AppProducts

  }
}
</script>

<style>
body {
  background-color: aliceblue;
  padding-top: 20px;
  padding-bottom: 20px;
}

.card {
  margin-right: 5px;
  margin-bottom: 5px;
}

.card:last-child {
  margin-right: 0px;
}

.col-md-2 {
  max-width: 15.666667% !important;
}

.product-container {
  margin-left: 15px;
}

.text-purple{
    color:#5f6c92;
}

</style>

