<template>
  <div class="hello">
    <div class="container" id="home-box">
      <h1>{{ msg }}</h1>
      <div class="columns">
        <div class="column">
          <router-link to="/ProductDetail">
            <div class="card">
              <div class="card-image is-4by3">
                <img src="./../assets/logo.png" alt="Placeholder image">
              </div>
              <div class="card-content">
                product name
              </div>
            </div>
          </router-link>
        </div>
        <div class="column">
          <router-link to="/ProductDetail">
            <div class="card">
              <div class="card-image is-4by3">
                <img src="./../assets/logo.png" alt="Placeholder image">
              </div>
              <div class="card-content">
                product name
              </div>
            </div>
          </router-link>
        </div>
        <div class="column">
          <router-link to="/ProductDetail">
            <div class="card">
              <div class="card-image is-4by3">
                <img src="./../assets/logo.png" alt="Placeholder image">
              </div>
              <div class="card-content">
                product name
              </div>
            </div>
          </router-link>
        </div>
        <div class="column">
          <router-link to="/ProductDetail">
            <div class="card">
              <div class="card-image is-4by3">
                <img src="./../assets/logo.png" alt="Placeholder image">
              </div>
              <div class="card-content">
                product name
              </div>
            </div>
          </router-link>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import './../../node_modules/bulma/css/bulma.css';

export default {
  name: 'Home',
  data () {
    return {
      msg: 'หน้าแรก สำหรับแสดงสินค้า'
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
nav {
  border-bottom: 10px;
}

#nav-top {
  border-bottom: 10px;
  border-color: #E0E0E0;
}

#nav-box {
  width: 1000px;
}

#home-box {
  background: white;
  width: 1000px;
  min-height: 2000px;
  margin-top: 13px;
  box-shadow: 2px 10px grey;
}




</style>
