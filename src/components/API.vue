<template>
    <div class="advice">
        {{ info }}
    </div>
</template>

<script>
import axios from 'axios'
export default{
  name: "API",
  data(){
      return{
          info: null
      }
  },
  mounted(){
      axios
        .get('https://api.adviceslip.com/advice')
        .then(response => (this.info = response))
  }
}

</script>
