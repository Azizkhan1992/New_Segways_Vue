<template>
  <div class="four-left-container">
    <h1>Packing List</h1>
    <div class="four-video">
      <div class="four-video-image" v-if="!isVideoActive">
        <svg
          width="80"
          height="81"
          viewBox="0 0 80 81"
          fill="none"
          xmlns="http://www.w3.org/2000/svg"
          @click="videoActive"
        >
          <g clip-path="url(#clip0_125_594)">
            <path
              d="M60.7508 39.5657L31.4175 19.5657C31.0082 19.2883 30.4802 19.2577 30.0428 19.4883C29.6068 19.719 29.3335 20.1723 29.3335 20.667V60.667C29.3335 61.1617 29.6068 61.615 30.0442 61.8457C30.2388 61.9497 30.4535 62.0003 30.6668 62.0003C30.9295 62.0003 31.1922 61.9217 31.4175 61.7683L60.7508 41.7683C61.1148 41.5203 61.3335 41.1083 61.3335 40.667C61.3335 40.2257 61.1148 39.8137 60.7508 39.5657ZM32.0002 58.143V23.191L57.6335 40.667L32.0002 58.143Z"
              fill="currentcolor"
            />
            <path
              d="M40 0.667114C17.944 0.667114 0 18.6111 0 40.6671C0 62.7231 17.944 80.6671 40 80.6671C62.056 80.6671 80 62.7231 80 40.6671C80 18.6111 62.056 0.667114 40 0.667114ZM40 78.0005C19.4147 78.0005 2.66667 61.2524 2.66667 40.6671C2.66667 20.0818 19.4147 3.33378 40 3.33378C60.5853 3.33378 77.3333 20.0818 77.3333 40.6671C77.3333 61.2524 60.5853 78.0005 40 78.0005Z"
              fill="currentcolor"
            />
          </g>
          <defs>
            <clipPath id="clip0_125_594">
              <rect
                width="80"
                height="80"
                fill="currentcolor"
                transform="translate(0 0.667114)"
              />
            </clipPath>
          </defs>
        </svg>
        <p>Нет перевода</p>
      </div>
      <div class="four-video-video" v-if="isVideoActive">
        <svg
          version="1.0"
          xmlns="http://www.w3.org/2000/svg"
          width="225.000000pt"
          height="225.000000pt"
          viewBox="0 0 225.000000 225.000000"
          preserveAspectRatio="xMidYMid meet"
          @click="videoActive"
        >
          <g
            transform="translate(0.000000,225.000000) scale(0.100000,-0.100000)"
            fill="currentcolor"
            stroke="none"
          >
            <path
              d="M993 2239 c-601 -70 -1046 -623 -984 -1220 29 -270 144 -512 333
-695 439 -427 1127 -427 1566 0 450 437 450 1165 0 1602 -182 177 -410 285
-661 313 -107 12 -149 12 -254 0z m544 -693 c90 -90 113 -119 113 -141 0 -23
-25 -53 -125 -154 l-124 -126 124 -126 c100 -101 125 -131 125 -154 0 -22 -23
-51 -113 -141 -62 -63 -119 -114 -126 -114 -8 0 -74 59 -148 132 l-133 132
-128 -127 c-88 -87 -136 -127 -151 -127 -30 0 -251 215 -251 244 0 13 47 68
130 151 l130 130 -130 130 c-84 84 -130 137 -130 151 0 29 221 244 250 244 15
0 66 -43 151 -127 l129 -127 133 132 c74 73 140 132 148 132 7 0 64 -51 126
-114z"
            />
          </g>
        </svg>
        <iframe
          src="https://player.vimeo.com/external/363012474.sd.mp4?s=aa2c1afbeedb4dd507cfd432f1546d0aa8e0152e&profile_id=164&oauth2_token_id=57447761"
          frameborder="0"
          width="100%"
          height="100%"
        ></iframe>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  name: "four-left",
  data() {
    return {
      isVideoActive: false,
    };
  },
  methods: {
    videoActive() {
      this.isVideoActive = !this.isVideoActive;
    },
  },
};
</script>
