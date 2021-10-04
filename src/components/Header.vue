<template>
  <div>
  <h1>{{ text }}</h1>
  <button @click="changeText">Ubah Text</button>
  </div>
</template>

<script>
export default {
props: ["text"],
data(){
        return {
            newText: "ini adalah text dari Header.vue"
        }
    },
    methods: {
        changeText(){
            this.$emit("ChangeTitle", this.newText);
        }
    }
}
</script>

<style>

</style>