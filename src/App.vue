<script setup>

</script>

<template>
  <div class="loader">
		<h1>Smart</h1>
</div>
</template>

<script>
export default {
  components: {
    
  },
  data() {
    return {
     
    };
  },
  methods: {
    
  }
};
</script>

<style scoped>

.loader{
	position: absolute;
	top: 50%;
	left: 50%;
	-webkit-transform: translate(-50%,-50%);
	   -moz-transform: translate(-50%,-50%);
	    -ms-transform: translate(-50%,-50%);
	     -o-transform: translate(-50%,-50%);
	        transform: translate(-50%,-50%);
}

.loader h1{
	margin: 0;
	padding: 0;
	font-size: 10em;
	color: rgba(255,255,255,.1);
	background-image: url(https://image.ibb.co/ciSeac/image.png);
	background-repeat: repeat-x;
	-webkit-background-clip: text;
	animation: animate 15s linear infinite;

}

@keyframes animate{
	0%{
		background-position: left 0px top 80px;
	}
	40%{
		background-position: left 800px top -50px;
	}
	80%{
		background-position: left 1800px top -50px;
	}
	100%{
		background-position: left 2400px top 80px;
	}
}
</style>
