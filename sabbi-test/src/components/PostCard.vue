<template>
  <div class="py block">
    <h2 class="text-center white text-h4 font-weight-bold underline">Post Content</h2>
    <v-container class="mt-10">
      <v-row>
        <v-col v-for="post, index in posts" :key="index" cols="4">
          <v-card class="card" style="border-radius: 1rem;" >
            <v-img
              cover
              height="250"
              :src='post.image'
            ></v-img>
        
            <v-card-item>
              <v-card-title class="font-weight-bold" style="text-transform: uppercase;">{{post.text}}</v-card-title>
            </v-card-item>
        
            <v-card-text>
              <v-row
                align="center"
                class="mt-5"
              >
              </v-row>
              <div class="d-flex justify-start p-2">
                <div>
                  <v-avatar size="50px">
                    <v-img
                    alt="Avatar"
                    :src="post.owner.picture"
                    ></v-img>
                  </v-avatar>
                </div>
                <div class="text-subtitle-1 px-4 mt-3 ">
                  {{post.owner.firstName + ' ' + post.owner.lastName }}
                </div>

              </div>
              <div class="d-flex justify-end">
                <v-icon>mdi-heart</v-icon>
                
                <div class="text-grey">
                  {{post.likes}}
                </div>
              </div>
            </v-card-text>
        
            <v-divider class="mx-4 mb-1"></v-divider>

              <v-card-title>Tags</v-card-title>
              <div class="px-2 pb-2">
                <v-chip-group v-model="selection">
                  <v-chip v-for="categoty, index in post.tags" :key="index" >{{categoty}}</v-chip>
                </v-chip-group>
              </div>


          </v-card>
        </v-col>
      </v-row>
    </v-container>
  </div>
</template>

<script>
import axios from 'axios'

export default {
    data () {
    return {
      posts: [],
      loading: true,
      errored: false
    }
  },
  filters: {
    currencydecimal (value) {
      return value.toFixed(2)
    }
  },
  mounted () {
    axios
      .get('https://dummyapi.io/data/v1/post?limit=6',
		{
			headers: {
        'app-id' : '637f53aaf75e03ede7f45e94'
			}
		}
      )
      .then(response => {
        this.posts = response.data.data
      })
      .catch(error => {
        console.log(error)
        this.errored = true
      })
      .finally(() => this.loading = false)
  }
}
</script>

<style scoped>
:hover.card{
  filter: drop-shadow(0 25px 25px rgb(0 0 0 / 0.15));
  transform: scale(1.05);
  transition-property: color, background-color, border-color, text-decoration-color, fill, stroke, opacity, box-shadow, transform, filter, backdrop-filter;
  transition-timing-function: cubic-bezier(0.4, 0, 0.2, 1);
  transition-duration: 150ms;
}

.underline{
  text-decoration-line: underline;
  text-underline-offset: 8px;
}
</style>