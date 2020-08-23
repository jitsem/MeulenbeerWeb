<template>
  <div id="home">
    <div id="header">
     <div id="bigLogo">
       <img alt="Meulenbeer logo" src="../assets/logo.png">
      </div>    
      <h1>Welcome to Meulenbeer Brewery</h1>
  </div>
    <div class="container">
      <h2>Who are we?</h2>
      <p>
          We are a father-and-son team of avid hobby-brewers. However don't let the hobby part fool you, 
          we take our work very seriues. Thanks to David and bradley to help us start on our journey.
          Also shoutout to BrewTools for making an awesome system.
      </p>
    </div>
    <p>
      Please check out our 
      <router-link to="/beers">Beers</router-link>      
    </p>
  </div>
</template>

<script>

export default {
  name: 'Home',
  components: {}
}
</script>

<style scoped>
#bigLogo {
  margin: 5px auto;
  width: 25%;  
}
#bigLogo img {
  width: 100%;
  max-width: 200px;
}

#header {
  margin-top: 5px;
  border: slategray 1px solid;
  border-radius: 15px;
  background: #e3e3e3;
}

#header h1 {
  text-align: center;
  margin: 5px 0;
}

.container {
  margin: 20px 0;
}

.container h2{
  margin-bottom: 5px;
}

</style>
