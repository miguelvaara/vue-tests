<script>
  export default {
    data() {
      return {
        uppercase: ''
      }
    },
    methods: {
        handleCustomChange (s) {
          this.uppercase = s
        }
    }
  }

</script>

<template>
  <my-text-input @custom-change="handleCustomChange" /> 
  <p>Uppercase: {{ uppercase }}</p>
</template>
