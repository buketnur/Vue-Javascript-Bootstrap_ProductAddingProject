<template>
    <div>
        <nav class="navbar navbar-expand-lg navbar-light bg-purple text-white mb-5">
  <a class="navbar-brand text-white" href="#">Ürün Ekleme Uygulaması | Vue.js | Buket Nur Astan </a>
  <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarNav" aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
    <span class="navbar-toggler-icon"></span>
  </button>
  <div class="collapse navbar-collapse" id="navbarNav">
    <ul class="navbar-nav">
      <li class="nav-item active">
        <a class="nav-link text-white" href="#">Eklenen Ürün <span class="badge badge-light">{{ navbarCount }}</span></a>
      </li>
    </ul>
  </div>
</nav>
    </div>
</template>

<script>
import { eventBus } from "../main"

export default {
    data : function (){
    return {
        navbarCount : 0
    }
},
    created(){
        eventBus.$on("progressBarUpdated", (productCount) => {
                this.navbarCount = productCount;
            });
            
    }

}

</script>

<style scoped>
.bg-purple{
    background-color:#8697cb;
}
.text-white{
    color: white;
}
</style>