<template>
  <h1 class="numbered-title"><span>01</span>Pick your destination</h1>
</template>

<script>
export default{
  data() {
    return{
      destinations:[],
    }
    
  },
  methods: {
    async loadData() {
      const response = await fetch(
        'https://space.wp.seiwald.hak-stjo.schulwebspace.at/wp-json/wp/v2/destination'
      )
      this.destinations = await response.json()
    }
  },
  mounted() {
    this.loadData()
    document.body.style.backgroundImage = "url('background-destination-mobile.jpg')"
  },
}
</script>


.ß
äÖ