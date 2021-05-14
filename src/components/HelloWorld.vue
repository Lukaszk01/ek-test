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
  name: 'HelloWorld',
  props: {
    msg: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
