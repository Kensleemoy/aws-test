<template>
    <div class="nav">
      <link href="https://fonts.googleapis.com/css2?family=Oswald&display=swap" rel="stylesheet">
      <ul>
          <a href="index.html">
            <li>
              HOME
            </li>
          </a>
          <a href="sources.html">
          <li>
              SOURCES
          </li>
            </a>
          <a href="about.html">
            <li id="bottom-nav">
                ABOUT US
            </li>
          </a>
      </ul>
    </div>
</template>

<script>
export default {
  name: 'Nav',
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.nav {
    height: 30%;
    text-align: left;
    width: 18%;
    margin-top: -20px;
    font-family: 'Oswald', sans-serif;
    position: absolute;
    z-index: 100;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: block;
  margin: 0;
  padding: 3%;
  background-color: #1c4587ff;
  color: #ffffffff;
  text-align: center;
}
a {
    text-decoration: none;
    color: #ffffffff;
    font-size: 35px;
}

li:hover {
    background-color: #ff9900;
    color: #1c4587ff
}

#bottom-nav {
  border-radius: 0px 0px 30px 30px;
  padding-bottom: 20px;
}
</style>
