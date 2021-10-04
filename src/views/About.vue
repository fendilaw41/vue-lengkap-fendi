<template>
  <div class="about">
    <h1>Berikut adalah data binding</h1>
    <a :href="url">GO TO facebook</a>
  </div>
</template>

<script>
export default {
  name: "About",
  data(){
    return {
      url: "https://facebook.com",
    }
  }
}
</script>