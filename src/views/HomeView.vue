<template>
  <div class="home">
    <div class="text-white">
      <Tweet v-for="tweet in tweets" :key="tweet._id" :tweet="tweet" />
    </div>
  </div>
</template>

<script>
import vuweets from '@/vuweets';
import { ref } from 'vue';
import Tweet from '@/components/VuWeet.vue';

export default {
  components: {
    Tweet,
  },
  setup () {
    const tweets = ref(vuweets);

    return {
      tweets,
      Tweet
    }
  }
}
</script>
