<template>
  <div class="twitter">
    <h4>LATEST FROM TWITTER</h4>
    <ul>
      <li v-for="(twit, index) in twits" :key="index">
        <Twit :details="twit"/>
      </li>
    </ul>
  </div>
</template>

<script>
  import Twit from './Twit.vue'

  export default {
    name: 'Twitter',
    components: {
      Twit
    },
    data() {
      return {
        twits: [
          {
            content: 'if you have any suggestions for the next updates, let us know.',
            date: '01:05 PM Sep 18th'
          },
          {
            content: 'We have just updated Porto Admin. Check the changelong for more information.',
            date: '01:04 PM Sep 18th'
          }
        ]
      }
    }
  }
</script>

<style lang="scss" scoped>  
  @import '../../assets/style/variables';

  h4{
    font-size: 20px;
    line-height: 20px;
    margin-bottom: 25px;
  }

</style>