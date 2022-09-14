<template>
  <div class="one-top-container">
    <div class="one-mobile-content">
        <button :class="{'right-hidden' : right_btn}" class="right" @click="slideRight">
          <svg
            width="8"
            height="29"
            viewBox="0 0 8 29"
            fill="none"
            xmlns="http://www.w3.org/2000/svg"
            
          >
            <path
              d="M1 1L6.37931 13.0667L7 14.4667L6.37931 15.8667L1 28"
              stroke="#009EFF"
              stroke-linecap="square"
            />
          </svg>
        </button>
      <div class="mobile-slide-wrapper"
      :style="{'margin-left': -moveRight + '%'}"
      >
        
        <div
          class="slide-items"
          v-for="slide in mobileSlideItems"
          :key="slide.id"
        >
          <img
            :src="require('@/assets/Content/ContentOne/Mobile/' + slide.img + '.svg')"
            alt=""
          />
          <p>{{ slide.name }}</p>
        </div>
      </div>
      <button :class="{'left-hidden' : left_btn}" class="left" @click="slideLeft">
          <svg
            width="8"
            height="29"
            viewBox="0 0 8 29"
            fill="none"
            xmlns="http://www.w3.org/2000/svg"
            
          >
            <path
              d="M1 1L6.37931 13.0667L7 14.4667L6.37931 15.8667L1 28"
              stroke="#009EFF"
              stroke-linecap="square"
            />
          </svg>
        </button>
    </div>
    <div class="one-top-content">
      <ul>
        <li>
          <a href="#">
            <img src="@/assets/Content/ContentOne/image1.svg" alt="" />
            Ks E22
          </a>
        </li>
        <li>
          <a href="#">
            <img src="@/assets/Content/ContentOne/image2.svg" alt="" />
            Ks Es1L
          </a>
        </li>
        <li>
          <a href="#">
            <img src="@/assets/Content/ContentOne/image3.svg" alt="" />
            Ks Air T15
          </a>
        </li>
        <li>
          <a href="#">
            <img src="@/assets/Content/ContentOne/image4.svg" alt="" />
            Ks F30
          </a>
        </li>
        <li>
          <a href="#">
            <img src="@/assets/Content/ContentOne/image5.svg" alt="" />
            Ks E45
          </a>
        </li>
        <li>
          <a href="#">
            <img src="@/assets/Content/ContentOne/image6.svg" alt="" />
            Ks Max
          </a>
        </li>
        <li>
          <a href="#">
            <img src="@/assets/Content/ContentOne/image7.svg" alt="" />
            Ks Max
          </a>
        </li>
      </ul>
    </div>
  </div>
</template>
<script>
export default {
  name: "one-top",
  data() {
    return {
        moveRight: 0,
        width: 25,
        counter: 0,
        right_btn: false,
        left_btn: false,
      mobileSlideItems: [
        { id: 1, img: "image1", name: "E22" },
        { id: 2, img: "image2", name: "ES1L" },
        { id: 3, img: "image3", name: "AIR T15" },
        { id: 4, img: "image4", name: "KS F30" },
        { id: 5, img: "image5", name: "KS E45" },
        { id: 6, img: "image6", name: "KS MAX" },
        { id: 7, img: "image7", name: "KS MAX" },
        { id: 8, img: "image8", name: "KS ES2" },
        { id: 9, img: "image9", name: "KS ES3" },
        { id: 10, img: "image10", name: "EKS ZING E12" },
        { id: 11, img: "image11", name: "KS ES4" },
        { id: 12, img: "image12", name: "EKS ZING E8" },
      ],
    };
  },
  methods:{
    slideRight(){
        if(this.counter < this.mobileSlideItems.length-4){
            this.counter++
            this.moveRight = this.width * this.counter
            this.left_btn = false
            
        }else{
            this.right_btn = true
        }
    },
    slideLeft(){
        if(this.counter>0){
            this.counter--
            this.moveRight = this.width * this.counter
            this.right_btn = false
        }else{
            this.left_btn = true
        }
    }
  }
};
</script>
