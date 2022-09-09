<template>
  <div class="content-twelwe-container">
    <div class="twelwe-content">
      <div class="twelwe-header">
        <h1>compare specifications</h1>
        <span>Add model to compare</span>
      </div>
      <div class="twelwe-slider">
        <button class="twelwe-right-btn" @click="runSlide" :disabled="slide_item_active">
          <svg
            width="70"
            height="71"
            viewBox="0 0 70 71"
            fill="none"
            xmlns="http://www.w3.org/2000/svg"
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
        <div class="twelwe-transparent"></div>
        <div
          class="slider-item"
          v-for="slide in slider_items"
          :key="slide.id"
          :id="slide.id"
          :class="{'active' : id_checker == slide.id  ,'active-left' :  slide_item_active && id_checker == slide.id }"
        >
          <img
            :src="
              require('@/assets/Content/ContentTwelwe/' + slide.img + '.svg')
            "
            alt=""
          />
          <p>{{ slide.name }}</p>
          <div
            :class="
              slide.active ? 'speed-title-active' : 'speed-title-deactive'
            "
          >
            <img
              src="@/assets/Content/ContentTwelwe/TwelweIcons/Vector1.svg"
              alt=""
            />
            <span>Max. speed</span>
          </div>
          <hr />
          <span class="slide-item-span">{{ slide.max_speed }}</span>
          <div
            :class="
              slide.active ? 'range-title-active' : 'range-title-deactive'
            "
          >
            <img
              src="@/assets/Content/ContentTwelwe/TwelweIcons/Vector2.svg"
              alt=""
            />
            <span>Range (miles)</span>
          </div>
          <hr />
          <span class="slide-item-span">{{ slide.range }}</span>
          <div
            :class="
              slide.active ? 'battery-title-active' : 'battery-title-deactive'
            "
          >
            <img
              src="@/assets/Content/ContentTwelwe/TwelweIcons/Vector3.svg"
              alt=""
            />
            <span>Battery Capacity</span>
          </div>
          <hr />
          <span class="slide-item-span">{{ slide.battery_cap }}</span>
          <div
            :class="
              slide.active ? 'weight-title-active' : 'weight-title-deactive'
            "
          >
            <img
              src="@/assets/Content/ContentTwelwe/TwelweIcons/Vector4.svg"
              alt=""
            />
            <span>Net Weight</span>
            
          </div>
          <hr />
          <span class="slide-item-span">{{ slide.net_weight }}</span>
          <div
            :class="
              slide.active ? 'payload-title-active' : 'payload-title-deactive'
            "
          >
            <img
              src="@/assets/Content/ContentTwelwe/TwelweIcons/Vector5.svg"
              alt=""
            />
            <span>Payload</span>
          </div>
          <hr />
          <span class="slide-item-span">{{ slide.payload }}</span>
          <div
            :class="slide.active ? 'time-title-active' : 'time-title-deactive'"
          >
            <img
              src="@/assets/Content/ContentTwelwe/TwelweIcons/Vector6.svg"
              alt=""
            />
            <span>Chargin Time</span>
          </div>
          <hr />
          <span class="slide-item-span">{{ slide.charge_time }}</span>
          <div
            :class="slide.active ? 'num-title-active' : 'num-title-deactive'"
          >
            <img
              src="@/assets/Content/ContentTwelwe/TwelweIcons/Vector7.svg"
              alt=""
            />
            <span>Number of Batteries</span>
          </div>
          <hr />
          <span class="slide-item-span">{{ slide.num_battery }}</span>
          <div
            :class="
              slide.active ? 'motor-title-active' : 'motor-title-deactive'
            "
          >
            <img
              src="@/assets/Content/ContentTwelwe/TwelweIcons/Vector8.svg"
              alt=""
            />
            <span>Motor power</span>
          </div>
          <hr />
          <span class="slide-item-span">{{ slide.motor_power }}</span>
          <div
            :class="
              slide.active ? 'power-title-active' : 'power-title-deactive'
            "
          >
            <img
              src="@/assets/Content/ContentTwelwe/TwelweIcons/Vector9.svg"
              alt=""
            />
            <span>Power Output</span>
          </div>
          <hr />
          <span class="slide-item-span">{{ slide.power_out }}</span>
          <div
            :class="
              slide.active ? 'incline-title-active' : 'incline-title-deactive'
            "
          >
            <img
              src="@/assets/Content/ContentTwelwe/TwelweIcons/Vector10.svg"
              alt=""
            />
            <span>Max. Incline</span>
          </div>
          <hr />
          <span class="slide-item-span">{{ slide.max_incline }}</span>
          <div
            :class="
              slide.active ? 'shock-title-active' : 'shock-title-deactive'
            "
          >
            <img
              src="@/assets/Content/ContentTwelwe/TwelweIcons/Vector11.svg"
              alt=""
            />
            <span>Shock Absorption</span>
          </div>
          <hr />
          <span class="slide-item-span">{{ slide.shock_abs }}</span>
          <div
            :class="
              slide.active ? 'safety-title-active' : 'safety-title-deactive'
            "
          >
            <img
              src="@/assets/Content/ContentTwelwe/TwelweIcons/Vector12.svg"
              alt=""
            />
            <span>Safety</span>
          </div>
          <hr />
          <span class="slide-item-span">{{ slide.safety }}</span>
          <div
            :class="
              slide.active ? 'light-title-active' : 'light-title-deactive'
            "
          >
            <img
              src="@/assets/Content/ContentTwelwe/TwelweIcons/Vector13.svg"
              alt=""
            />
            <span>Atmosphere Light</span>
          </div>
          <hr />
          <span class="slide-item-span">{{ slide.atmosphere_light }}</span>
          <h4>{{ slide.price }}</h4>
          <button>BUY IT NOW</button>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  name: "content-twelwe",
  data() {
    return {
        id_checker: 1,
        id_checker_left: 1,
        slide_item_active: false,
      slider_items: [
        {
          id: 1,
          active: true,
          name: "nininebot kickscooter e22",
          img: "image1",
          max_speed: "20 км/ч",
          range: "22 км",
          battery_cap: "5100 mAh",
          net_weight: "13.5 кг",
          payload: "25 кг - 100 кг",
          charge_time: "3.5 часа",
          num_battery: "1 встроенная",
          motor_power: "Номинальная 300W",
          power_out: "71W (0.071kW)",
          max_incline: "15%",
          shock_abs: "----",
          safety: "Задний LED-фонарь",
          atmosphere_light: "----",
          price: "$599.99",
        },
        {
          id: 2,
          name: "NiNinebot Kickscooter ES1l",
          img: "image2",
          max_speed: "20 км/ч",
          range: "20 км",
          battery_cap: "184 mAh",
          net_weight: "10.3 кг",
          payload: "25 кг - 100 кг",
          charge_time: "6 часов",
          num_battery: "1 встроенная",
          motor_power: "Номинальная 250W",
          power_out: "42W (0.042kW)",
          max_incline: "7%",
          shock_abs: "Передняя",
          safety: "----",
          atmosphere_light: "----",
          price: "$389.99",
        },
        {
          id: 3,
          name: "NiNinebot Kickscooter Air T15",
          img: "image3",
          max_speed: "20 км/ч",
          range: "12 км",
          battery_cap: "4000 mAh",
          net_weight: "10.5 кг",
          payload: "30 кг - 100 кг",
          charge_time: "4 часа",
          num_battery: "1 встроенная",
          motor_power: "Номинальная 300W",
          power_out: "71W (0.071kW)",
          max_incline: "15%",
          shock_abs: "----",
          safety: "Задний LED-фонарь",
          atmosphere_light: "----",
          price: "$819.99",
        },
        {
          id: 4,
          name: "NiNinebot Kickscooter f30",
          img: "image4",
          max_speed: "25 км/ч",
          range: "30 км",
          battery_cap: "7650 mAh",
          net_weight: "15.1 кг",
          payload: "30 кг - 120 кг",
          charge_time: "5 часов",
          num_battery: "1 встроенная",
          motor_power: "Номинальная 300W",
          power_out: "71W (0.070kW)",
          max_incline: "15%",
          shock_abs: "----",
          safety: "Задний LED-фонарь",
          atmosphere_light: "----",
          price: "$649.99",
        },
        {
          id: 5,
          name: "NiNinebot Kickscooter ZING E8",
          img: "image5",
          max_speed: "30 км/ч",
          range: "35 км",
          battery_cap: "7650 mAh",
          net_weight: "15.5 кг",
          payload: "35 кг - 120 кг",
          charge_time: "5 часов",
          num_battery: "1 встроенная",
          motor_power: "Номинальная 300W",
          power_out: "71W (0.070kW)",
          max_incline: "10%",
          shock_abs: "----",
          safety: "Задний LED-фонарь",
          atmosphere_light: "----",
          price: "$599.99",
        },
        {
          id: 6,
          name: "nininebot kickscooter MAX",
          img: "image6",
          max_speed: "30 км/ч",
          range: "40 км",
          battery_cap: "10200 mAh",
          net_weight: "17.5 кг",
          payload: "30 кг - 100 кг",
          charge_time: "6.5 часов",
          num_battery: "1 встроенная",
          motor_power: "Номинальная 350W Максимальная 700W",
          power_out: "121 W",
          max_incline: "15%",
          shock_abs: "----",
          safety: "Задний LED-фонарь",
          atmosphere_light: "----",
          price: "$599.99",
        },
        {
          id: 7,
          name: "NiNinebot Kickscooter es2",
          img: "image7",
          max_speed: "25 км/ч",
          range: "25 км",
          battery_cap: "187 Wh  ",
          net_weight: "12.5 кг",
          payload: "25 кг - 100 кг",
          charge_time: "3.5 часа",
          num_battery: "1 встроенная",
          motor_power: "Номинальная 350W Максимальная 700W",
          power_out: "71W ",
          max_incline: "10%",
          shock_abs: "----",
          safety: "Задний LED-фонарь",
          atmosphere_light: "----",
          price: "$599.99",
        },
        {
          id: 8,
          name: "NiNinebot Kickscooter es3",
          img: "image8",
          max_speed: "25 км/ч",
          range: "45 км",
          battery_cap: "374 Wh  ",
          net_weight: "13.6 кг",
          payload: "25 кг - 100 кг",
          charge_time: "7 часов",
          num_battery: "2",
          motor_power: "Номинальная 250W Максимальная 600W",
          power_out: "71W ",
          max_incline: "15%",
          shock_abs: "----",
          safety: "Cветодиодная фара, боковые и задние отражатели",
          atmosphere_light: "----",
          price: "$599.99",
        },
        {
          id: 9,
          name: "NiNinebot Kickscooter es4",
          img: "image9",
          max_speed: "30 км/ч",
          range: "45 км",
          battery_cap: "374 Wh  ",
          net_weight: "14 кг",
          payload: "25 кг - 100 кг",
          charge_time: "7 часов",
          num_battery: "2",
          motor_power: "Номинальная 300W Максимальная 800W",
          power_out: "71W ",
          max_incline: "15%",
          shock_abs: "----",
          safety: "Задний LED-фонарь",
          atmosphere_light: "----",
          price: "$699.99",
        },
        {
          id: 10,
          name: "NiNinebot Kickscooter e45",
          img: "image10",
          max_speed: "30 км/ч",
          range: "45 км",
          battery_cap: "10200 mAh",
          net_weight: "16.4 кг",
          payload: "25 кг - 100 кг",
          charge_time: "7.5 часов",
          num_battery: "1 встроенная",
          motor_power: "Номинальная 300W",
          power_out: "71W (0.070kW)",
          max_incline: "20%",
          shock_abs: "----",
          safety: "Задний LED-фонарь",
          atmosphere_light: "----",
          price: "$499.99",
        },
      ],
    };
  },
  methods: {
    runSlide(){

      this.slide_item_active = true
       setTimeout(()=>{
      this.slideDelay()
      this.slide_item_active = false
       }, 1500)
            
       
    },
    slideDelay(){
      let first_item = this.slider_items.shift()
            this.slider_items.push(first_item)
            this.id_checker_left = first_item.id

        if(this.id_checker == this.slider_items.length){
            this.id_checker = 1
            this.slider_items.forEach(item => {
                if(item.id == this.id_checker){
                    item.active = true
                }else{
                    item.active = false
                }
            })
        }else{
            this.id_checker++
            this.slider_items.forEach(item => {
                if(item.id == this.id_checker){
                    item.active = true
                }else{
                    item.active = false
                }
            })
        }
    }
  }
};
</script>
