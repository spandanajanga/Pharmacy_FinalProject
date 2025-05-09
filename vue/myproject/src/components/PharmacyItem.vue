<template>

   
   

   

<div class="medicine-box">
    <h2>{{ medicine.medicine }}</h2>
    <h3>Category: {{ medicine.category }}</h3>
    <h3>Price: ${{ medicine.price }}</h3>
    <h3>In Stock: {{ medicine.stock_quantity }}</h3>
    <h4>Manufactured: {{ medicine.manufacturing_date }}</h4>
    <h4>Expires: {{ medicine.expiration_date }}</h4>
  </div>
   
 
 </template>
 
 <script>
 
 export default {
  name: 'PharmacyItem',

   props: {
     medicine: Object
   }
 }
 
 </script>
 
 
 <style scoped>

 .green{
     background-color: green;
 }
 
 h4{
     margin: 2px;
 }
 
 div{
     background-color: #b3d7f4;
     color: black;
     padding: 1em;
     text-align: center;
     width: 80%;
     margin: auto;
     box-shadow: auto;
     
 
 }
 
 .red{
 background-color: orangered !important;
 
 }
 
 
 </style>