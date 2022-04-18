<template>
  <div class="gb--content">
    <div class="gb--content__advice">
      <h1>advice #{{ id }}</h1>

      <span>{{ advice }}</span>
      <br />
      <svg width="444" height="16" xmlns="http://www.w3.org/2000/svg">
        <g fill="none" fill-rule="evenodd">
          <path fill="#4F5D74" d="M0 8h196v1H0zM248 8h196v1H248z" />
          <g transform="translate(212)" fill="#CEE3E9">
            <rect width="6" height="16" rx="3" />
            <rect x="14" width="6" height="16" rx="3" />
          </g>
        </g>
      </svg>
      <br />
      <button @click="getAdvice" class="change">
        <svg width="24" height="24" xmlns="http://www.w3.org/2000/svg">
          <path
            d="M20 0H4a4.005 4.005 0 0 0-4 4v16a4.005 4.005 0 0 0 4 4h16a4.005 4.005 0 0 0 4-4V4a4.005 4.005 0 0 0-4-4ZM7.5 18a1.5 1.5 0 1 1 0-3 1.5 1.5 0 0 1 0 3Zm0-9a1.5 1.5 0 1 1 0-3 1.5 1.5 0 0 1 0 3Zm4.5 4.5a1.5 1.5 0 1 1 0-3 1.5 1.5 0 0 1 0 3Zm4.5 4.5a1.5 1.5 0 1 1 0-3 1.5 1.5 0 0 1 0 3Zm0-9a1.5 1.5 0 1 1 0-3 1.5 1.5 0 0 1 0 3Z"
            fill="#202733"
          />
        </svg>
      </button>
    </div>
    <footer>
      <div class="attribution">
        Challenge by
        <a href="https://www.frontendmentor.io?ref=challenge" target="_blank"
          >Frontend Mentor</a
        >. Coded by <a href="https://github.com/GabrielaMRs">Gabriela Rodrigues</a>.
      </div>
    </footer>
  </div>
</template>

<script>
import axios from "axios";

export default {
  name: "MyGenerator",
  components: { axios },
  data() {
    return {
      id: "",
      advice: "",
    };
  },
  mounted() {
      axios
        .get("https://api.adviceslip.com/advice")
        .then(response => { this.advice = response.data.slip.advice; 
                            this.id = response.data.slip.id;})
  },
  methods:{
    getAdvice(){
      window.location.reload();
    }
  }
};
</script>

<style>
</style>