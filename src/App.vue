<template>
     <router-view></router-view>
      <div class="footer">
        <div class="row text-left">
          <ul id="fo">
            <li class="term-of-service">Terms of Service</li>
            <li class="contact-us">Contact Us</li>
            <li><img src="@/assets/facebook.svg" alt=""></li>
            <li class=""><img src="@/assets/instagram.svg" alt=""></li>
            <li class=""><img src="@/assets/tweeter.svg" alt=""></li>
            <li class=""><img src="@/assets/soundcloud.svg" alt=""></li>
            <li class=""><img src="@/assets/spotify.svg" alt=""></li>
          </ul>  
        </div>
      </div>
</template>


<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

.modal {
  width: 250px;
  height: 200px;
  padding: 10px;
  margin: 0 auto;
  margin-top: 20px;
  border-radius: 2%;
  background-color: #e0e0e0;
}


.term-of-service {
  margin-left: 20px;
}
.footer {
  height: 40px;
  background: #1A1B35;
  font-family: Roboto-Regular;
  font-size: 12px;
  color: rgba(255,255,255,0.87);
  text-align: left;
  position: fixed;
  bottom: 0px;
  width: 100%;
}
.footer li {
  display: inline-block;
  margin-right: 15px;
  margin-top: 10px;
}
.social-media {
  margin-left: 1120px;
}
.social-media li {
  margin-right: 30px;
  margin-left: 0px;
}
#fo {
  display: inline-block;
  width: 100%;
}

@media only screen and (max-width: 600px) {
  .footer {
    height: 80px;
  }
  li img {
    margin-left: 35px;
    margin-top: 5px;
    margin-bottom: 10px;

  }
  li.contact-us {
    margin-right: 170px;
  }
}
@media only screen and (min-width: 768px) {
  li img {
    margin-right: 8px;
  }
  li.contact-us {
    margin-right: 48%;
  }

}
@media only screen and (min-width: 992px) {
  li.contact-us {
  margin-right: 69%;
}
}
</style>
