<template>
  <MyHeader Name="PHARMACY" authorName="SPANDANA JANGA" />
  <PharmacyBox :pharmacy="pharmacy" />
</template>

<script>
import MyHeader from './components/MyHeader.vue'
import PharmacyBox from './components/PharmacyBox.vue'

export default {
  name: 'App',
  components: {
    MyHeader,
    PharmacyBox
  },
  data() {
    return {
      pharmacy: []
    }
  },
  created() {
    this.fetchPharmacy()
  },
  methods: {
    async fetchPharmacy() {
      const res = await fetch("https://spandanajanga-nodejs.onrender.com/api");
      const data = await res.json();
      console.log(data);
      this.pharmacy = data;
    }
  }
}
</script>




<style>


@import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@300&display=swap');
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

body {
  font-family: 'Montserrat', sans-serif;
}
.container {
  max-width: 400px;
  margin: 30px auto;
  overflow: auto;
  min-height: 300px;
  border: 0.3em solid black;
  padding: 30px;
  border-radius: 5px;
}

div{
  margin-bottom: 0.5em;
  text-align: center;
}


</style>