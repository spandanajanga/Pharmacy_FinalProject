<template>

    <h2> {{ Name }}</h2>
    <h3> {{ authorName }}</h3>
</template>

<script>

export default {
  name: 'MyHeader',
  props: {
    Name: String,
    authorName: String
  }
}

</script>


<style scoped>

div{
    text-align: center;
}

</style>