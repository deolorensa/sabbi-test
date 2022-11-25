<template>
  <div>
    <v-container>
      <v-row>
        <v-col class="d-flex justify-center align-center" cols="6">
          <div>
            <h1 class="text-left white">Welcome to Technical Test <br> Can I Help You ?</h1>
            <br>
            <div>
              <v-btn class="button">
                Make User ?
              </v-btn>
            </div>
          </div>
        </v-col>
        <v-col cols="6">
          <lottie-player src="https://assets8.lottiefiles.com/packages/lf20_ioxlu1zt.json"  background="transparent"  speed="1"  style="width: 500px; height: 500px;"  loop autoplay></lottie-player>
        </v-col>
      </v-row>
    </v-container>
  </div>
  <PostCard id="post" />

</template>

<script>

import { defineComponent } from 'vue';

// Components
import PostCard from '@/components/PostCard.vue';

export default defineComponent({
  name: 'HomeView',

  components: {
    PostCard,
  },
});
</script>

<style scoped>

.button{
  padding: 10px 50px;
  background-color: white;
  text-align: center;
  border-radius: 25px;
}
:hover.button{
  background-color: rgb(0, 115, 255);
  color: aliceblue;
}
</style>