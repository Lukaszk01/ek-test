<template>
      <article class="series-card" :class="{ 'is-favorite': isFavorite }">
    <router-link class="series-card-link" :to="showUrl">
      <div class="container">
        <div class="single-show">
          <div class="row">
            <div class="image">
              <img class="series-card-poster" :src="showImage" :alt="item.show.name" />
            </div>
            <div class="container">
              <div class="row">
                <div class="info">
                    <header class="series-card-header">
                      <h2 class="series-card-title mt-3">{{ item.show.name }}</h2>
                        <h2 class="series-card-summary">{{ item.show.summary.replace(reg, "") }}</h2>
                        <h3 class="genre"><b>Genre: </b></h3>
                        <div class="series-genres">
                          <div
                            class="series-genres-item"
                            v-for="genre in item.show.genres"
                            :key="genre"
                            >
                            <div>{{ genre }}</div>
                        </div>
                        <div><b>Runtime: </b>{{ item.show.runtime}}min</div>
                      </div>
                  </header> 
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
      
      

      


      
    </router-link>
  </article>
</template>

<script>
import { defineComponent } from '@vue/composition-api'

export default defineComponent({
    setup() {
        
    },
})
</script>

<style>


</style>
