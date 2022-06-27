<template>
  <div>
    <button @click="removeLike" style="margin-right: 10px">-</button>
    <span>Likes: {{ likes }}</span>
    <button @click="addLike" style="margin-left: 10px">+</button>
  </div>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      likes: 0,
    }
  },
  methods: {
    addLike() {
      this.likes += 1
    },
    removeLike() {
      if (this.likes > 0) this.likes -= 1
      else console.log('Отрицательного количества не может быть')
    }
  }
}
</script>

<style scoped>

</style>