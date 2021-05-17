<template>
  <article class="series-card" :class="{ 'is-favorite': isFavorite }">
    <!-- <router-link class="series-card-link" :to="item.show.url"> -->
    <transition name="fade">
      <div class="container">
        <div v-if="show" class="single-show">
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
                        <h3 class="genre"><b>Genre:</b></h3>
                        <div class="series-genres">
                        <div class="series-genres-item" 
                          v-for="genre in item.show.genres" :key="genre">
                            <div>{{ genre }}</div>
                        </div>
                        <div><b>Runtime: </b>{{ item.show.runtime}}min</div>
                        <div><b>Show's link: </b>{{item.show.url}}</div>
                      </div>
                  </header> 
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
      
    </transition>
    <!-- </router-link> -->
  </article>
</template>

<script>
  // const regex = /<[^>]*>/gm
import { favoriteStorage } from "../store";
export default {
  props: {
    item: {
      type: Object
    }
  },
  data() {
    return {
      show: true,
      reg: /<[^>]*>/gm,
      favoriteShows: favoriteStorage.fetch(),
      isFavorite: null,
    };
  },
  created() {
    this.setIsFavoriteInitialValue();
  },
  computed: {
    showUrl() {
      return `/show/${this.item.show.id}`;
    },
    showImage() {
      return this.item.show.image
        ? this.item.show.image.medium
        : "images/no-image.png";
    }
  },
  methods: {
    setIsFavoriteInitialValue() {
      this.isFavorite = !!this.favoriteShows[this.item.show.id];
    },
  }
};
</script>

<style>

.container {
  animation: fadeIn 3s;
  -webkit-animation: fadeIn 3s;
  -moz-animation: fadeIn 3s;
  -o-animation: fadeIn 3s;
  -ms-animation: fadeIn 3s;
}
@keyframes fadeIn {
  0% {opacity:0;}
  100% {opacity:1;}
}

@-moz-keyframes fadeIn {
  0% {opacity:0;}
  100% {opacity:1;}
}

@-webkit-keyframes fadeIn {
  0% {opacity:0;}
  100% {opacity:1;}
}

@-o-keyframes fadeIn {
  0% {opacity:0;}
  100% {opacity:1;}
}

@-ms-keyframes fadeIn {
  0% {opacity:0;}
  100% {opacity:1;}
}


Resources
.fade-enter-active,
.fade-leave-active {
  transition: opacity 0.9s ease;
}

.fade-enter-from,
.fade-leave-to {
  opacity: 0;
}
  .single-show {
    width: 1100px;
    height: 300px;
    border-radius: 20px;
    font-size: 20px;
    color: rgba(0,0,0,0.87);
    text-align: left;
    font-family: Roboto-Medium;
    background: #D6D8E7;
    margin-bottom: 20px;
    word-wrap: break-word;
    overflow: auto;
    transition: 2s;
  }
  .single-show:hover {
    width: 1200px;
    height: 400px;
    transition: 2s;
    padding: 20px
  }
  .series-card-poster {
    border-radius: 25px;
    height: 300px;
    width: 200px;
    opacity: 0.7;
    padding: 20px;
    object-fit: fill;
    margin: 0px;
  }

  .row>* {
    width: 30%;
    margin-left: 0px;
  }
  .info p {
    font-family: Roboto-Medium;
    font-size: 12px;
    color: rgba(0,0,0,0.87);
    text-align: left;
    margin: 50px;
    width: 800px;
  }
  ul {
    font-size: 12px;
  }
  .series-card-title {
    text-decoration: none;
    width: 500px;

  }
  a {
    text-decoration: none;
  }
  .image {
    margin-right: -140px;
  }
  .series-card-summary {
    font-size: 16px;
    width: 800px;
    word-wrap: break-word;
  }
  .series-genres {
    white-space: nowrap;
  }
  .series-genres-item {
    font-weight: normal;
  }
  .genre {
    width: 200px;
    font-size: 20px;
  }
</style>