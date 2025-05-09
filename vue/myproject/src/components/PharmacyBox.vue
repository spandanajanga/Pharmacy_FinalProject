<template>

  

   <div>

        <PharmacyItem
        v-for="item of pharmacy" :key="item.id" :medicine ="item"/> 

   </div>
    
   


</template>

<script>


import PharmacyItem from './PharmacyItem.vue'

export default {
  name: 'pharmacyBox',
  props: {
   pharmacy: Array
  },
  components: {
    PharmacyItem
  },
}

</script>


<style scoped>
.medicine-box {
  color: black;
  padding: 1em;
  text-align: center;
  width: 80%;
  margin: 20px auto; 
  box-shadow: 0px 4px 6px rgba(0, 0, 0, 0.1);
  border-radius: 8px;
}

.medicine-box:nth-child(odd) {
  background-color: #fce4ec; 
}

.medicine-box:nth-child(even) {
  background-color: #e3f2fd; 
}

h4 {
  margin: 2px;
}
</style>
