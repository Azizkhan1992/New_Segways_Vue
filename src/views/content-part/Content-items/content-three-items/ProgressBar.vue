<template>
  <div class="progres-items">
    <div class="progres-items-content">
      <div v-for="(header, idx) in progres_headers" :key="idx"
        :class="header.active ? 'header-active' : 'header-deactive'"
      >
        <button @click="setProgresTab(header.value)">
          <svg width="38" height="37" viewBox="0 0 38 37" fill="currentcolor" xmlns="http://www.w3.org/2000/svg" v-html="header.svg"></svg>
          <div class="header-title">{{ header.title }}</div>
          
        </button>
      </div>
    </div>
    <slot :active="activeProgres" />
  </div>
</template>
<script>
export default {
  name: "progres-items",
  props: {
    headers: {
      type: Array,
      default: () => [],
    },
  },
  data() {
    return {
      progres_headers: [],
    };
  },
  computed: {
    activeProgres() {
      return this.progres_headers.length > 0
        ? this.progres_headers.find((item) => item.active).value
        : null;
    },
  },
  mounted() {
    this.initHeaders();
  },
  methods: {
    setProgresTab(tabValue) {
      this.progres_headers = this.progres_headers.map((item) => {
        item.active = false;

        if (item.value === tabValue) {
          item.active = true;
        }
        return item;
      });
    },
    initHeaders() {
      this.progres_headers = this.headers.map((item) => {
        item.active = !!item.active;
        return item;
      });
    },
  },
};
</script>
