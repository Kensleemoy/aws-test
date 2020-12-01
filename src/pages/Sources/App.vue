<template>
  <div id="app">
    <link href="https://fonts.googleapis.com/css2?family=Oswald&display=swap" rel="stylesheet">
    <Header/>
    <h1>SOURCES</h1>
    <div class="horizontal-container">
    <hr /> 
	<div class="source">
		<span class = "subhead">DATA VALIDITY STATEMENT  </span> Data is presented directly from our API source. More information on their data sources can be found here:
		<a href="https://docs.google.com/presentation/d/1XmKCBWYZr9VQKFAdWh_D7pkpGGM_oR9cPjj-UrNdMJQ/edit#slide=id.g91040bbb51_413_0" target="_blank" rel="noopener">
			Covid Act Now - data sources </a>
	</div>
	<div class="source">
		<span class = "subhead">API  </span> <a href="https://covidactnow.org/resources#api" target="_blank" rel="noopener">covidactnow.org</a>
	</div>
	<div class="source">
      <span class = "subhead">MAP  </span>  <a href="https://github.com/VictorCazanave/svg-maps" target="_blank" rel="noopener">Idaho Map</a>
  </div>
   </div>
	</div>
</template>

<script>

export default {
	name: 'Sources',
	components: {
		Header: () => import('@/components/Header.vue'),
	},
 
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
.horizontal-container{
	text-align: left;
}
.source{
	margin: 20px;
}
</style>
