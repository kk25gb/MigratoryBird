<template>
  <div class="container-fluid myCarousel">

    <div id="carouselExampleControls" class="carousel slide" data-ride="carousel">
      <div class="carousel-inner">
        <div class="carousel-item pic1 active">
          
        </div>
        <div class="carousel-item pic2">
         
        </div>
        <div class="carousel-item pic3">
         
        </div>
      </div>
      <a class="carousel-control-prev" href="#carouselExampleControls" role="button" data-slide="prev">
        <span class="carousel-control-prev-icon" aria-hidden="true"></span>
        <span class="sr-only">Previous</span>
      </a>
      <a class="carousel-control-next" href="#carouselExampleControls" role="button" data-slide="next">
        <span class="carousel-control-next-icon" aria-hidden="true"></span>
        <span class="sr-only">Next</span>
      </a>
    </div>

    <!-- <Brief_InfoBar></Brief_InfoBar> -->
  </div>
</template>

<script>
// import HouseDTHeader from "../components/HouseDTHeader";
// import Brief_InfoBar from '../components/Brief_InfoBar';
export default {
  name: "Carousel",
  components: {
    // HouseDTHeader,
    // Brief_InfoBar,
  },
  data() {
    return {
      isShow_hiddenNav: false
    };
  },
  methods: {
    show_hiddenNav: function() {
      this.isShow_hiddenNav = !this.isShow_hiddenNav;
    }
  }
};
</script>

<style lang="scss" scoped>
@mixin size($w, $h) {
  width: $w;
  height: $h;
}
*{
  padding: 0px;
}
.carousel {
  .carousel-inner {
    .carousel-item {
      @include size($w: 100vw, $h: 100vh);
      background-repeat: no-repeat;
      background-size: cover;
      background-position: 0% 40%;
    }
    .pic1 {
      background-image: url("../assets/media/pic_MB01.jpg");
    }
    .pic2 {
      background-image: url("../assets/media/pic_MB02.jpg");
    }
    .pic3 {
      background-image: url("../assets/media/pic_MB03.jpg");
    }
  }
  .carousel-control-prev, .carousel-control-next{
    z-index: 0;
  }
  .carousel-control-prev-icon,.carousel-control-next-icon {
    // position: relative;
    filter: invert(100%);
  }
}
</style>
