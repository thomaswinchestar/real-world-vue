<!-- eslint-disable vue/multi-word-component-names -->
<template>
  <p>Register the event here</p>
  <button @click="register">Register Me</button>
</template>

<script>
export default {
  props: ['event'],
  inject: ['GStore'],
  methods: {
    register() {
      // call to API
      // if registered then redirect to event details

      this.GStore.flashMessage =
        'You are successfullly registered for ' + this.event.title

      setTimeout(() => {
        this.GStore.flashMessage = ''
      }, 3000)

      this.$router.push({
        name: 'EventDetails',
      })
    },
  },
}
</script>
