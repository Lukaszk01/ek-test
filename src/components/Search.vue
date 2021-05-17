<template>
<div class="alert">
  <span class="closebtn" onclick="this.parentElement.style.display='none';">&times;</span>
  Congratulations! You have been successfully logged in!!
</div>

<div class="button-login mt-3 ml-3"><router-link class="link" to="/">LOGOUT</router-link></div>
  <transition name="fade">
    <router-view />
  </transition>
  <div>
    <form @submit.prevent="emitQuery">
      <label for="search-form__input">Find your TV show!</label>
      <input
        id="search-form__input"
        type="search"
        autocomplete="off"
        v-model="query"/>
      <button @click="show = !show">Search</button>
    </form>
  </div>

</template>

<script>
export default {
  data() {
    return {
      show: false,
      query: this.getInitialQueryValue()
    };
  },
  watch: {
    $route() {
      this.query = this.getInitialQueryValue()
    }
  },
  methods: {
    getInitialQueryValue() {
      return this.$route.query.search || "";
    },
    emitQuery() {
      this.$emit("submit:query", this.query);
    },
    myFunction() {
      var close = document.getElementsByClassName("closebtn");
      var i;
      for (i = 0; i < close.length; i++) {
        close[i].onclick = function(){
        var div = this.parentElement;
        div.style.opacity = "0";
        setTimeout(function(){ div.style.display = "none"; }, 600);
        }
      }
    }
  }
};
</script>
<style>
.fade-enter {
  opacity: 0;
}
.fade-enter-active,
.fade-leave-active {
  transition: opacity 2s ease-out;
}
.fade-leave-to {
  opacity: 0;
}
.slide-fade-enter {
  transform: translateX(10px);
  opacity: 0;
}
.slide-fade-enter-active,
.slide-fade-leave-active {
  transition: all 2s ease;
}
.slide-fade-leave-to {
  transform: translateX(-10px);
  opacity: 0;
}
.alert {
  padding: 20px;
  background-color: #1A1B35; /* Red */
  color: white;
  font-family: Roboto-Medium;
  margin-bottom: 15px;
  transition-delay: 3s;
}
/* The close button */
.closebtn {
  margin-left: 15px;
  color: white;
  font-weight: bold;
  float: right;
  font-size: 22px;
  line-height: 20px;
  cursor: pointer;
  transition: 0.3s;
}
/* When moving the mouse over the close button */
.closebtn:hover {
  color: black;
}
a {
color: white
  }
a:hover {
  color: #b8b9e3;
}
.button-login {
  margin-left: 5px;
}
</style>