<template>
  <div id="stateData">
	<div><span class = "subhead">Last updated on: </span> {{state.lastUpdatedDate}}</div>
	<div><span class = "subhead">Population: </span> {{state.population}}</div>
	<div><span class = "subhead">Cases: </span>{{state.actuals.cases}}</div>
	<div><span class = "subhead">Deaths:</span> {{state.actuals.deaths}}</div>
	<div><span class = "subhead">Hospital Beds: </span>{{state.actuals.hospitalBeds.capacity}}</div>
	<div><span class = "subhead">Hospital beds used by Covid:</span> {{state.actuals.hospitalBeds.currentUsageCovid}}</div>
	<div><span class = "subhead">ICU Beds:</span> {{state.actuals.icuBeds.capacity}}</div>
	<div><span class = "subhead">ICU beds used by Covid:</span> {{state.actuals.icuBeds.currentUsageCovid}}</div>
	
  </div>
</template>

<script>
  export default {
    name: 'StateData',
	data(){
		return{
			state: {
        actuals: {
          hospitalBeds: {

          },
          icuBeds: {

          },
        },
      },
	}
	},
	mounted() {
		this.getStateData()
	},
	methods: {
		async getStateData(){
			try {
				const proxyurl = "https://hidden-fortress-01637.herokuapp.com/"; 
				const url = "https://api.covidactnow.org/v2/state/ID.json?apiKey=";
				const key = process.env.VUE_APP_APIKEY;
				const response = await fetch (proxyurl + url+ key);
        const data = await response.json();
        this.state = JSON.parse(JSON.stringify(data));
			} catch (error) {
				console.error(error);
			}
		},
	}
  }
</script>

<style scoped>
	button {
		margin: 0 0.5rem 0 0;
	}
	input {
		margin: 0;
	}
	.empty-table {
		text-align: center;
	}
</style>