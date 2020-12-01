<template>
    <div>
        <link href="https://fonts.googleapis.com/css2?family=Oswald&display=swap" rel="stylesheet">
        <div class="header">
            <a href="index.html"><h1><span id="COV-ID">COV-ID</span><span id="aho">aho</span></h1></a>
        </div>
        <Nav /> 
    </div>
</template>

<script>
export default {
  name: 'Header',
  components: {
      Nav: () => import('@/components/Nav.vue'),
  },
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

.header {
    text-align: center;
    background-color: #1c4587ff;
    height: 20%;
    width: 100%;
    padding-top: 1%;
    padding-bottom: 5px;
    position: relative;
    font-family: 'Oswald', sans-serif;
}
h1 {
    font-size: 60px;
}
#COV-ID {
    color: #ff9900;
}

#aho {
    color: #ffffff;
    font-weight: bold;
}
a {
    text-decoration: none;
}

Nav {
    float: top;
}
</style>
