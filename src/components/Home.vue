<template>
<div class="split left">
  <div class="centered">
    <img class="planet" src="@/assets/Image.png" style="width: 700px height: 1050px" alt="">
    <!-- <img class="image" src="@/assets/logInPageImage.svg" alt=""> -->
    <div class="logo"> <p>LOGO</p> </div>
  </div>
</div>
<div class="split right col-12">
  <header class="text-left"> <p>LOGO</p> </header>
  <div class="centered-right">
    <div class="container">
      <h1>Log in</h1>
        <p class="log-inf">Email Address</p>
          <div class="position-relative d-flex flex-row-reverse flex-lg-row flex-wrap flex-lg-nowrap flex-justify-center flex-lg-justify-between pt-6 pb-2 mt-6 f6 text-gray border-top border-gray-light mt-3 mb-3 ml-1"></div>
        <p class="log-inf">Password</p>
          <div class="position-relative d-flex flex-row-reverse flex-lg-row flex-wrap flex-lg-nowrap flex-justify-center flex-lg-justify-between pt-6 pb-2 mt-6 f6 text-gray border-top border-gray-light mt-3 mb-3 ml-1"></div>
    </div>
    <div class="container">
      <div class="row text-center">
          <div class="col">
            <div class="d-flex justify-content-between">
              <div class="d-flex justify-content-start">
                <div class="checkbox"></div>
                <p class="log-inf ml-3">REMEBER ME</p>
              </div>
            <p class="forgot-password justify-content-end">Forgot Password</p>
          </div>
        </div>
      </div>
      </div>
        <div class="container">
          <div class="row text-center">
            <div class="col">
              <div class="d-flex justify-content-between">
                <div class="button-cancel text-center mt-3">CANCEL</div>
                <div class="button-login mt-3"><router-link class="link" to="/main">LOGIN</router-link></div>
              </div>
            </div>
          </div>
        </div>
        <div class="container">
          <div class="row text-center">
            <div class="col">
              <div class="d-flex justify-content-end">
                <div class="thin-text p-3">Don't have account yet?</div>
                <div class="sign-up p-3">Sign Up here</div>
              </div>
            </div>
          </div>
        </div>
    </div>
  </div>
</template>

<script>

export default {
  name: 'home',
  props: {
    msg: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>


.split {
  height: 100%;
  width: 50%;
  position: fixed;
  top: 0;
  /*padding-top: 20px;*/
  overflow: hidden;
}


.right {
  right: 0;
  background-color: #ffff;
  display: flex;
}

.centered-right {
  position: absolute;
  top: 25%;
  left: 50%;
  transform: translate(-50%, 0%);
  text-align: center;
}
.centered {
  position: absolute;
  top: 25%;
  left: 50%;
  transform: translate(-50%, 0%);
  text-align: center;
}
.centered img {
  width: 1130px;
  z-index: 2;
  position: absolute;
  top: -310px;
  left: -334px;
  display: flex;
}
.button-cancel {
  width: 100px;
  height: 30px;
  background: #1A1B35;
  border-radius: 100px;
  font-family: Roboto-Medium;
  font-size: 12px;
  color: #FFFFFF;
  text-align: center;
  padding: 5px;

}
.button-login {
  width: 100px;
  height: 30px;
  background-image: linear-gradient(132deg, #62419A 0%, #3E76EB 100%);
  border-radius: 100px;
  font-family: Roboto-Medium;
  font-size: 12px;
  color: #FFFFFF;
  text-align: center;
  padding: 5px;
}
.checkbox {
  background: #FFFFFF;
  border: 1px solid #CCCCCC;
  border-radius: 2px;
  width: 15px;
  height: 15px;
}

.log-inf {
  font-family: Roboto-Medium;
  font-size: 12px;
  color: rgba(0,0,0,0.87);
  text-align: left;
}
.thin-text {
  font-family: Roboto-Light;
  font-size: 12px;
  color: rgba(0,0,0,0.87);
  text-align: right;
}
.link {
  color: #fff;
  text-decoration: none;
}
/*transition animation*/

.modal {
  width: 250px;
  height: 200px;
  padding: 10px;
  margin: 0 auto;
  margin-top: 20px;
  border-radius: 2%;
  background-color: #e0e0e0;
}
/*** TRANSITIONS ***/
.fade-enter {
  opacity: 0;
}
.fade-enter-active,
.fade-leave-active {
  transition: opacity 0.5s ease-out;
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
  transition: all 0.2s ease;
}
.slide-fade-leave-to {
  transform: translateX(-10px);
  opacity: 0;
}
.container {
  width: 500px;
}
.forgot-password {
  font-family: Roboto-Light;
  font-size: 12px;
  color: rgba(0,0,0,0.87);
  text-align: left;
  text-decoration: underline;
}
.sign-up {
  font-family: Roboto-Light;
  font-size: 12px;
  color: rgba(0,0,0,0.87);
  text-align: right;
  text-decoration: underline;
}
.link {
  font-family: Roboto-Medium;
  font-size: 12px;
  color: #FFFFFF;
  text-align: center;
  padding: 5px;
}
h1 {
  font-family: Roboto-Medium;
  font-size: 20px;
  color: rgba(0,0,0,0.87);
  text-align: center;
  margin-bottom: 50px;
}
.planet {
  position: absolute;
  overflow: hidden;

}
.contained img {
  width: 50%;
}
.logo {
  background: #1A1B35;
  border-radius: 13px;
  font-family: Roboto-Medium;
  color: #FFFFFF;
  
  display: flex;
  position: relative;
  border: 1px solid black;
  height: 75px;
  width: 75px;
  z-index: 2;
  bottom: 245px;
  opacity: 1;
  right: 220px;
  align-items: center;
  justify-content: center;

}
.logo p {
  margin-top: 10px;
  font-size: 20px;
}
header {
  background: #1A1B35;
  height: 40px;
  font-family: Roboto-Regular;
  top: 0px;
  width: 100%;
}
/*RESPONSIVE VERSIONS*/
@media only screen and (max-width: 600px) {
  .centered img {
  width: 1130px;
  
  z-index: 2;
  position: absolute;
  top: -310px;
  left: -334px;
  display: none
}
  [class*="col-"] {
    width: 100%;
  }
  .container {
    width: 350px;
  }
  header {
  height: 40px;
  top: 0px;
  width: 100%;
  background: #222222;

  font-family: Roboto-Regular;
  font-size: 20px;
  color: #FFFFFF;
  text-align: left;
}
header p {
  margin-left: 15px;
}

}

@media only screen and (min-width: 768px) {
/*  .split {
    width: 100%;
  }
  .container {
    width: 350px;
  }*/
  .centered img {
  width: 1130px;
  
  z-index: 2;
  position: absolute;
  top: -310px;
  left: -334px;
  display: none
}
  [class*="col-"] {
    width: 100%;
  }
  header {
  background: #1A1B35;
  height: 40px;
  top: 0px;
  width: 100%;

  font-family: Roboto-Regular;
  font-size: 20px;
  color: #FFFFFF;
  text-align: left;
}
header p {
  margin-left: 10px;
}
}
@media only screen and (min-width: 992px) {
  .centered img {
    display: flex;
  }
  [class*="col-"] {
    width: 50%;
  }
  header {
  background: #1A1B35;
  height: 40px;
  font-family: Roboto-Regular;
  top: 0px;
  width: 100%;
  display: none;
}
}


</style>
