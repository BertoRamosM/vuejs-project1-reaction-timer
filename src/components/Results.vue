 <template>
     <p >Reaction time: {{ reactionTime }}ms</p>
     <p class="rank">{{ rank }}</p>
 </template>
 
 <script>
export default {
  props: ['reactionTime'],
  data() {
    return {
      rank: null
    }
  },
  mounted() {
    if (this.reactionTime < 250) {
      this.rank = "Ninja fingers!"
    } else if (this.reactionTime < 400) {
      this.rank = "Rapid reflexes"
    } else {
      this.rank = "Snail pace..."
    }
  }
}
 </script>
 
 <style>
 .rank{
  font-size: 1,4rem;
  color: #0faf87;
  font-weight: bold;
 }
 </style>