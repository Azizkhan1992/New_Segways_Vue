<template>
  <div class="two-slider-container">
    <div class="slider-wrapper">
      <div
        class="slider-items"
        v-for="slider in slider_items"
        :key="slider.id"
        :id="slider.id"
        :class="
          id_checker == slider.id
            ? 'active'
            : '' || id_checker_left == slider.id
            ? 'left'
            : ''
        "
      >
        <img
          :src="
            require('@/assets/Content/ContentTwo/TwoSlider/' +
              slider.img +
              '.svg')
          "
          alt=""
        />
      </div>
    </div>
    <div class="dot-btn">
      <button
        v-for="btn in slider_items"
        :key="btn.id"
        @click="active_item(btn.id)"
        :class="btn.id == dot ? 'active-btn' : ''"
      ></button>
    </div>
  </div>
</template>
<script>

export default {
  name: "two-slider",
  data() {
    return {
      id_checker: 1,
      id_checker_left: 1,
      dot: 1,
      slider_items: [
        { id: 1, img: "slider1" },
        { id: 2, img: "slider2" },
        { id: 3, img: "slider3" },
        { id: 4, img: "slider4" },
        { id: 5, img: "slider5" },
        { id: 6, img: "slider6" },
        { id: 7, img: "slider7" },
      ],
    };
  },
  mounted() {
    this.autoplay();
    this.move_dot()
  },
  methods: {
    play() {
      const slideLen = this.slider_items.length;
      let first_item = this.slider_items.shift();
      this.slider_items.push(first_item);

      if (this.id_checker == slideLen) {
        this.id_checker = 1;
      } else {
        this.id_checker++;
      }

      if (this.id_checker_left == slideLen) {
        this.id_checker_left = 1;
      } else {
        this.id_checker_left++;
      }
    },
    autoplay() {
      this.id_checker_left = this.slider_items.length;
      setInterval(() => {
        this.play();
      }, 3000);
    },
    active_item(e) {
      this.id_checker = e;
    },
    move_dot(){
        this.slider_items.forEach(item => {
            this.dot = item.id
        })
    }
  },
};
</script>
