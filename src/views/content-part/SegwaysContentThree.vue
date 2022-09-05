<template>
  <div class="progres-bar-container">
    <div class="progres-bar-content">
      <progress-bar :headers="ProgresHeaders" v-slot="slotProps">
        <div v-for="(head, idx) in ProgresHeaders" :key="idx">
          <div :class="head.active ? 'tab-header-active' : 'tab-header-deactive'">
            <div class="tab-1" v-if="slotProps.active == 'one'">
              <div class="tab-1-left">
                <h1>We are in Los Angeles, CA</h1>
                <p>Free California 1 day shipping. US Free Shipping 3-5 Days</p>
              </div>
              <div class="tab-1-right">
                <img
                  src="@/assets/Content/ContentThree/ContentThreeItems/tab1.svg"
                  alt=""
                />
              </div>
            </div>
            <div class="tab-2" v-if="slotProps.active == 'two'">
              <div class="tab-2-left">
                <h1>After Sales Support</h1>
                <p>
                  If you have any difficulties with your kickscooter, our
                  spealists will contact you within 15 minutes
                </p>
              </div>
              <div class="tab-2-right">
                <img
                  src="@/assets/Content/ContentThree/ContentThreeItems/tab2.svg"
                  alt=""
                />
              </div>
            </div>
            <div class="tab-3" v-if="slotProps.active == 'three'">
              <div class="tab-3-left">
                <h1>One year manufacturer's warranty</h1>
                <p>
                  The basic warranty is 1 year. You can also extend the warranty
                  up to 4 years
                </p>
              </div>
              <div class="tab-3-right">
                <img
                  src="@/assets/Content/ContentThree/ContentThreeItems/tab3.svg"
                  alt=""
                />
              </div>
            </div>
            <div class="tab-4" v-if="slotProps.active == 'four'">
              <div class="tab-4-left">
                <h1>Up to 40 miles of range on a single charge</h1>
                <p>With a range of up to 40 miles, the longest range on the market, and a 20˚uphill climbing angle, the KickScooter MAX allows you to ride from San Francisco Bay Area to Palo Alto on a single charge.</p>
              </div>
              <div class="tab-4-right">
                <img src="@/assets/Content/ContentThree/ContentThreeItems/tab4.svg" alt="">
              </div>
            </div>
          </div>
        </div>
      </progress-bar>
    </div>
  </div>
</template>
<script>
import ProgressBar from "./Content-items/content-three-items/ProgressBar.vue";
export default {
  name: "progres-bar",
  components: { ProgressBar },
  data() {
    return {
      ProgresHeaders: [
        {
          name: "Active",
          title: "Delivery within 1 business day",
          img: "img1",
          value: "one",
          active: true,
        },
        {
          name: "Inactive",
          title: "Basic 1 year warranty",
          img: "img2",
          value: "two",
        },
        {
          name: "Inactive",
          title: "After Sales Support",
          img: "img3",
          value: "three",
        },
        {
          name: "Inactive",
          title: "Up to 40 miles per charge",
          img: "img4",
          value: "four",
        },
      ],
    };
  },
};
</script>
