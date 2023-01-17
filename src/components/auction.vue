<template>
  <div class="auction">
    <div class="auction__inside">
      <div class="auction__left_static">
        <div class="auction__top">
          <div class="auction__text"> Auctions <br /> ending <br /> soon </div>
        </div>

        <div class="auction__bottom">
          <div class="auction__text2">explorer more</div>
        </div>
      </div>

      <div class="auction__right_dynamic">
        <div class="slider">
          <swiper
            :slides-per-view="1"
            :space-between="0"
            @swiper="onSwiper"
            @slideChange="onSlideChange"
          >
            <swiper-slide v-for="i in 4">
              <div class="auction__item">
                <img
                  src="../assets/img/home1.webp"
                 
                  class="auctuin__background absolute -z-10"
                />
                <div class="auction__crator">
                  <div class="auction__profile">
                    <img
                      class="auction__image"
                      src="https://picsum.photos/500/500"
                    />
                  </div>
                  <div class="auction__name">@randomdash</div>
                </div>
                <div class="auction__item__content">
                  <div class="auction__frame-99">
                    <div class="auction__frame-62">
                      <div class="auction__current-bid">Current bid</div>

                      <div class="auction__frame-52">
                        <div class="auction___8-00-eth">8.00 ETH</div>

                        <div class="auction__-24-635-39">$24,635.39</div>
                      </div>
                    </div>

                    <div class="auction__frame-63">
                      <div class="auction__auction-ends-in">
                        Auction ends in
                      </div>

                      <div class="auction__frame-55">
                        <div class="auction__frame-52">
                          <div class="auction___23">23</div>

                          <div class="auction__hours">hours</div>
                        </div>

                        <div class="auction__frame-53">
                          <div class="auction___59">59</div>

                          <div class="auction__minutes">minutes</div>
                        </div>

                        <div class="auction__frame-54">
                          <div class="auction___59">59</div>

                          <div class="auction__seconds">seconds</div>
                        </div>
                      </div>
                    </div>
                  </div>
                </div>
              </div>
            </swiper-slide>
          </swiper>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
// Import Swiper Vue.js components
import { Swiper, SwiperSlide } from "swiper/vue";

// Import Swiper styles
import "swiper/css";

export default {
  components: {
    Swiper,
    SwiperSlide,
  },
  setup() {
    const onSwiper = (swiper) => {
      console.log(swiper);
    };
    const onSlideChange = () => {
      console.log("slide change");
    };
    return {
      onSwiper,
      onSlideChange,
    };
  },
};
</script>
