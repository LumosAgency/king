<template>
  <div class="carousel">
    <div class="carousel__top">
      <h3>A whisker worthy experience</h3>
      <div class="carousel__buttons">
        <button @click="showPrev" class="carousel__buttons__left">
          <span>Previous</span>
          <i></i>
        </button>
        <button @click="showNext" class="carousel__buttons__right">
          <span>Next</span><i></i>
        </button>
      </div>
    </div>
    <VueSlickCarousel v-bind="slickOptions" ref="carousel">
      <div class="inner-slide">
        <img
          src="~/assets/img/gallery_img_1.png"
          alt="Photo of cats playing in a large space"
        />
      </div>
      <div class="inner-slide">
        <img
          src="~/assets/img/gallery_img_2.png"
          alt="Photo of cats playing in a large space"
        />
      </div>
      <div class="inner-slide">
        <img
          src="~/assets/img/gallery_img_3.png"
          alt="Photo of cats playing in a large space"
        />
      </div>
      <div class="inner-slide">
        <img
          src="~/assets/img/gallery_img_1.png"
          alt="Photo of cats playing in a large space"
        />
      </div>
      <div class="inner-slide">
        <img
          src="~/assets/img/gallery_img_2.png"
          alt="Photo of cats playing in a large space"
        />
      </div>
      <div class="inner-slide">
        <img
          src="~/assets/img/gallery_img_3.png"
          alt="Photo of cats playing in a large space"
        />
      </div>
    </VueSlickCarousel>
  </div>
</template>
  
  <script>
import VueSlickCarousel from 'vue-slick-carousel'

export default {
  name: 'MyComponent',
  components: { VueSlickCarousel },
  data() {
    return {
      slickOptions: {
        slidesToShow: 3,
        arrows: false,
        dots: false,
        autoplay: true,
        swipe: false,
        responsive: [
          {
            breakpoint: 1000,
            settings: {
              slidesToShow: 2,
            },
          },
          {
            breakpoint: 767,
            settings: {
              slidesToShow: 1,
              swipe: true,
            },
          },
        ],
      },
    }
  },
  methods: {
    showNext() {
      this.$refs.carousel.next()
    },
    showPrev() {
      this.$refs.carousel.prev()
    },
  },
}
</script>