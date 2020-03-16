<template lang="pug">
  .event-show
    h1 Show Event 
    | #
    | {{ id }} Event
</template>

<script>
export default {
  props: ['id']
}
</script>

<style></style>
