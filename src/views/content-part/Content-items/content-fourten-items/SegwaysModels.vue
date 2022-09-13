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
          <input type="text" class="number-input" placeholder="+998-" @keypress="keyIn($event)" v-model="phone_number">
          <input type="text">
          <button>SEND</button>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  name: "segways-models",
  data(){
    return{
      phone_number: null
    }
  },
  methods:{
    keyIn(e){
      const charCode = e.which ? e.which : e.keyCode;
      this.phoneIn(e)
      if(charCode > 31 && (charCode < 48 || charCode > 57) && charCode !== 46){
        e.preventDefault()
        
      }else{
        if(this.phone_number?.length == 2){
          this.phone_number = '+' + this.phone_number
        }
      }
      
    },
    phoneIn(evt){
      let num = evt.target.value
      if(num && this.phone_number.length == 12){
        let part = this.phone_number.split("")
         console.log(part)
      }
    }
  }
};
</script>
