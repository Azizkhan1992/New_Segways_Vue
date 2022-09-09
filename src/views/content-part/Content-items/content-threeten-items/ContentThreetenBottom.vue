<template>
  <div class="threeten-bottom">
    <h1>REviews</h1>
    <button
    class="left-one-btn"
        @click="moveLeft"
        :disabled="checker_left_two">

      <svg
        width="70"
        height="71"
        viewBox="0 0 70 71"
        fill="none"
        xmlns="http://www.w3.org/2000/svg"
        class="svg-left"
      >
        <g clip-path="url(#clip0_216_4049)">
          <path
            d="M1.4001 69.5996L68.6001 69.5996L68.6001 2.39961L1.40011 2.39961L1.4001 69.5996Z"
            fill="currentcolor"
          />
          <path
            d="M2.8 68.1L2.80001 3.69999L67.2 3.7L67.2 68.1L2.8 68.1ZM0 71L70 71L70 1L6.11959e-06 0.999994L0 71Z"
            fill="currentcolor"
          />
          <path
            d="M25.9002 38.1002L44.1002 56.2002L46.2002 54.1002L28.1002 36.0002L46.2002 17.8002L44.1002 15.7002L25.9002 33.9002L23.8002 36.0002L25.9002 38.1002Z"
            fill="currentcolor"
          />
        </g>
        <defs>
          <clipPath id="clip0_216_4049">
            <rect
              width="70"
              height="70.1"
              fill="white"
              transform="translate(70 71) rotate(-180)"
            />
          </clipPath>
        </defs>
      </svg>
    </button>
    <div class="threeten-slider">
      <div class="slider-wrapper-one">
        <div
          class="slide-items-one"
          :class="{'active' : checker_right_one == slide.id && checker_right_two , 'left' : checker_left_one == slide.id && checker_left_two}"
          v-for="slide in slideItems"
          :key="slide.id"
          :id="slide.id"
        >
          <img :src="require('@/assets/Content/ContentThreeten/' + slide.img + '.svg')" alt="" />
        </div>
      </div>
    </div>
    <button
    class="right-one-btn"
        @click="moveRight"
        :disabled="checker_right_two">

      <svg
        width="70"
        height="70"
        viewBox="0 0 70 70"
        fill="none"
        xmlns="http://www.w3.org/2000/svg"
        class="svg-right"
      >
        <path
          d="M68.5999 1.40039H1.3999V68.6004H68.5999V1.40039Z"
          fill="currentcolor"
        />
        <path
          d="M67.2 2.9V67.3H2.8V2.9H67.2ZM70 0H0V70H70V0Z"
          fill="currentcolor"
        />
        <path
          d="M44.0998 32.8998L25.8998 14.7998L23.7998 16.8998L41.8998 34.9998L23.7998 53.1998L25.8998 55.2998L44.0998 37.0998L46.1998 34.9998L44.0998 32.8998Z"
          fill="currentcolor"
        />
      </svg>
    </button>
  </div>
</template>
<script>
export default {
  name: "threeten-bottom",
  data() {
    return {
        checker_right_one: 1,
        checker_right_two: false,
        checker_left_one: 1,
        checker_left_two: false,
      slideItems: [
        { id: 1, img: "img2" },
        { id: 2, img: "img2" },
        { id: 3, img: "img2" },
        { id: 4, img: "img2" },
        { id: 5, img: "img2" },
      ],
    };
  },
  methods: {
    moveRight(){
        this.checker_right_two = true
        setTimeout(()=> {
            this.slideMoveOne()
            this.checker_right_two = false
        },1500)
    },
    slideMoveOne(){
        let first_item = this.slideItems.shift()
        this.slideItems.push(first_item)
        this.checker_right_one = this.slideItems[0].id
    },
    moveLeft(){
        this.checker_left_two = true
        this.slideMoveTwo()
        setTimeout(()=>{
            this.checker_left_two = false
        }, 1500)
    },
    slideMoveTwo(){
        let last_item = this.slideItems.pop()
        this.slideItems.unshift(last_item)
        this.checker_left_one = this.slideItems[0].id
        this.checker_right_one = this.checker_left_one
    }
  }
};
</script>
