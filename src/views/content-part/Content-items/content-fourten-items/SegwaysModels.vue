<template>
  <div class="segways-models">
    <div class="segways-models-content">
      <div class="models-header">
        <h1>OTHER MODELS</h1>
        <span>Check out the entire line of Segway scooters</span>
      </div>
      <div class="models-content">
        <div class="model-items">
          <div class="model-img">
            <div class="model-circle">
              <img
                src="@/assets/Content/ContentFourten/Models/image1.svg"
                alt=""
              />
            </div>
          </div>
          <div class="model-title">
            <h3>KS E22</h3>
            <p>$899.99</p>
            <button>SEE MORE</button>
          </div>
        </div>
        <div class="model-items">
          <div class="model-img">
            <div class="model-circle">
              <img
                src="@/assets/Content/ContentFourten/Models/image2.svg"
                alt=""
              />
            </div>
          </div>
          <div class="model-title">
            <h3>KS ES1l</h3>
            <p>$389.99</p>
            <button>SEE MORE</button>
          </div>
        </div>
        <div class="model-items">
          <div class="model-img">
            <div class="model-circle">
              <img
                src="@/assets/Content/ContentFourten/Models/image3.svg"
                alt=""
              />
            </div>
          </div>
          <div class="model-title">
            <h3>KS Air t15</h3>
            <p>$819.99</p>
            <button>SEE MORE</button>
          </div>
        </div>
        <div class="model-items">
          <div class="model-img">
            <div class="model-circle">
              <img
                src="@/assets/Content/ContentFourten/Models/image4.svg"
                alt=""
              />
            </div>
          </div>
          <div class="model-title">
            <h3>KS F30</h3>
            <p>$649.99</p>
            <button>SEE MORE</button>
          </div>
        </div>
        <div class="model-items">
          <div class="model-img">
            <div class="model-circle">
              <img
                src="@/assets/Content/ContentFourten/Models/image5.svg"
                alt=""
              />
            </div>
          </div>
          <div class="model-title">
            <h3>KS E45</h3>
            <p>$859.99</p>
            <button>SEE MORE</button>
          </div>
        </div>
        <div class="model-items">
          <div class="model-img">
            <div class="model-circle">
              <img
                src="@/assets/Content/ContentFourten/Models/image6.svg"
                alt=""
              />
            </div>
          </div>
          <div class="model-title">
            <h3>KS MAX</h3>
            <p>$949.99</p>
            <button>SEE MORE</button>
          </div>
        </div>
        <div class="model-items">
          <div class="model-img">
            <div class="model-circle">
              <img
                src="@/assets/Content/ContentFourten/Models/image7.svg"
                alt=""
              />
            </div>
          </div>
          <div class="model-title">
            <h3>MKS MAX</h3>
            <p>$949.99</p>
            <button>SEE MORE</button>
          </div>
        </div>
        <div class="model-items find-model">
          <h2>DIDN'T FIND A MODEL?</h2>
          <p>Leave your contact details and we will help you with the choice</p>
          <input
            type="text"
            class="number-input"
            placeholder="998  "
            @keypress="keyIn($event)"
            v-model="phone_number"
          />
          <input type="text" />
          <button>SEND</button>
        </div>
      </div>

      <div class="fourten-mobile-carousel">
        <div class="mobile-carousel-content">
          <div class="mobile-transparent"></div>
          <div class="mobile-carousel-wrapper">
            
        
            <div
              class="fourten-carousel-items"
              v-for="slide in fourtenCarousel"
              :key="slide.id"
              :id="slide.id"
              :class="{
                'fourten-active': slide.id == activeId,
                'fourten-left': slide.id == activeLeft,
              }"
            >
              <div class="fourten-circle">
                <img
                  :src="
                    require('@/assets/Content/ContentFourten/Models/' +
                      slide.img +
                      '.svg')
                  "
                  alt=""
                />
              </div>
              <h2>{{ slide.name }}</h2>
              <p>{{ slide.price }}</p>
              <button>SEE MORE</button>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  name: "segways-models",
  data() {
    return {
      fourtenCarousel: [
        {
          id: 1,
          img: "image1",
          name: "NineboT KICKSCOOTER E22",
          price: "33 900 руб",
        },
        {
          id: 2,
          img: "image2",
          name: "NineboT KICKSCOOTER ES1l",
          price: "33 900 руб",
        },
        {
          id: 3,
          img: "image3",
          name: "KS Air t15",
          price: "$819.99",
        },
        {
          id: 4,
          img: "image4",
          name: "KS F30",
          price: "$649.99",
        },
        {
          id: 5,
          img: "image5",
          name: "KS E45",
          price: "$859.99",
        },
        {
          id: 6,
          img: "image6",
          name: "KS MAX",
          price: "$949.99",
        },
        {
          id: 7,
          img: "image7",
          name: "MKS MAX",
          price: "$949.99",
        },
      ],
      activeId: 1,
      activeLeft: 1,
      phone_number: null,
    };
  },
  mounted() {
    this.runCarousel();
  },
  methods: {
    runCarousel() {
      this.activeLeft = this.fourtenCarousel.length;
      setInterval(() => {
        let item = this.fourtenCarousel.shift();
        this.fourtenCarousel.push(item);

        if (this.activeId >= this.fourtenCarousel.length) {
          this.activeId = 1;
        } else {
          this.activeId++;
        }

        if (this.activeLeft >= this.fourtenCarousel.length) {
          this.activeLeft = 1;
        } else {
          this.activeLeft++;
        }
      }, 3000);
    },
    keyIn(e) {

      const pattern = /(\d{0,3})(\d{0,2})(\d{0,3})(\d{0,2})(\d{0,2})/
            let phone = e.target.value.replace(/\D/g, '').match(pattern)
            
            e.target.value = '';

            for (let i = 1; i < 6; i++) {
                e.target.value += phone[i] != '' ? (i == 1 ? '+' : '-') + phone[i] : '';
            }

    },
    phoneIn(evt) {
      let num = evt.target.value;
      if (num && this.phone_number.length == 12) {
        let part = this.phone_number.split("");
        console.log(part);
      }
    },
  },
};
</script>
