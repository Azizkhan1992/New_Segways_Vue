<template>
  <div class="five-carousel-container">
    <div class="five-carousel-content">
      <div class="five-carousel-wrapper">
        <div
          class="five-carousel-items"
          v-for="slide in five_carousel"
          :key="slide.id"
          :id="slide.id"
          :class="{'carousel-active' : slide.id == currentId , 'carousel-left' : slide.id == leftId }"
        >
          <div class="carousel-circle">
            <img
              :src="
                require('@/assets/Content/ContentFive/' + slide.img + '.svg')
              "
              alt=""
            />
          </div>
          <h4>{{ slide.title }}</h4>
          <p>{{ slide.description }}</p>
          <span>Price: {{ slide.price }}</span>
          <button>ADD TO CART</button>
        </div>
      </div>
    </div>
  </div>
</template>
<script>

export default {
  name: "five-carousel",
  data() {
    return {
        currentId: 1,
        leftId: 1,
      five_carousel: [
        {
          id: 1,
          img: "image1",
          title: "NineboT Engine Speaker",
          description:
            "The built-in engine sound simulation system can simulate the realistic engine roar based on the vehicle's accelerator, brake, speed, and other signals",
          price: "$149.99",
        },
        {
          id: 2,
          img: "image2",
          title: "Extension Rod",
          description:
            "The Extension Rod helps you to easily maneuver your scooter, so you no longer need to bend over and push it, making it easier to take with you anywhere.",
          price: "$149.99",
        },
        {
          id: 3,
          img: "image3",
          title: "Segway Protective Gear Set",
          description:
            "The curved, streamlined design of the helmet shell, coupled with the thick, high-quality fabrics create a helmet that is stylish, protective and comfortable to wear.",
          price: "$29.99",
        },
        {
          id: 4,
          img: "image4",
          title: "Ninebot Leisure Backpack",
          description:
            "The Ninebot leisure backpack adopts a stylish gray-yellow color contrast, adding a trendy accessory to your wardrobe.",
          price: "$69.99",
        },
        {
          id: 5,
          img: "image5",
          title: "Segway External Battery",
          description:
            " It is easy to install and increases the range of the ES1, ES2 & E22 to 27.9, 28 and 27 miles respectively and It also increases the speed",
          price: "$249.99",
        },
        {
          id: 6,
          img: "image6",
          title: "Segway Charger",
          description:
            "Whether at home, the office, or on your KickScooter journey, this Ninebot KickScooter by Segway Charger is designed to provide a safe and stable charge anytime, anywhere.",
          price: "$79.99",
        },
        {
          id: 7,
          img: "image7",
          title: "Segway Scoter Bag",
          description:
            "Tough EVA material, suitable for the entire Ninebot KickScooter by Segway line. 3L capacity gives you plenty of room to carry your phone, charger, bottled water, and other personal items.",
          price: "$49.99",
        },
        {
          id: 8,
          img: "image8",
          title: "Segway Phone Holder",
          description:
            "The dual screw, non-slip design offers ultimate security and versatility. The phone holder is applicable to multiple vehicle series.",
          price: "$29.99",
        },
        {
          id: 9,
          img: "image9",
          title: "SegwayPhone Holder",
          description:
            "This scooter seat is designed to work with the MAX. It offers high quality, comfort and safety that is in line with the MAX KickScooter.",
          price: "$119.99",
        },
      ],
    };
  },
  mounted(){
    this.moveSlide()
  },
  methods: {
    moveSlide() {
      this.leftId = this.five_carousel.length
        setInterval(() => {
          if(this.currentId <=this.five_carousel.length-1){
            this.currentId++
          }else{
            this.currentId=1
          }
          if(this.leftId >= this.five_carousel.length){
            this.leftId = 1
          }else{
            this.leftId++
          }
          let item = this.five_carousel.shift();
          this.five_carousel.push(item);
    }, 3000);
    },
  },
};
</script>
