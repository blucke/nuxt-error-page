<template>
  <div>
  	<h1 v-if="error.statusCode === 404">{{ message }}</h1>
  	<h5>{{ number }}</h5>
  	<h3>{{ title }}</h3>
    <h2>Back to
      <nuxt-link to="/">Home</nuxt-link>
    </h2>
  	<h4>{{ note }}</h4>
  </div>
</template>

<script>
export default {
  props: ['error'],
  layout: 'error',
  data() {
  	return {
  	  message: 'Upsss!',
  	  number: '404',
  	  title: 'Page Not Found',
  	  note: 'Sorry but the page you are looking for doesn\'t exist.'
  	}
  },
  head() {
  	return {
  		title: 'Error 404 Page',
  		meta: [
  		  { hid: 'Error Page with Nuxt.js', name: 'Error 404', content: 'Error 404 Page with Nuxt.js'}
  		]
  	}
  }
}
</script>

<style>
h3 {
  color: rgba(255, 255, 255, 0.8);
  text-align: center;
  font-size: 3em;
}
h4 {
  font-size: 1em;
  color: rgba(255, 255, 255, 0.4);
  text-align: center;
}
h2 {
  text-align: center;
  color: rgba(0, 0, 0, 0.5);
}	
</style>