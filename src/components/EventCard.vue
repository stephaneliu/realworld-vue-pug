<template lang="pug">
  router-link.event-link(
    :to="{ name: 'event-show', params: { id: '1' } }"
  )
    .event-card.-shadow
      span.eyebrow @{{ event.time }} on {{ event.date }} &nbsp;
      h4.title {{ event.title }}
      BaseIcon(name="users") {{ event.attendees.length }} attending
</template>

<script>
export default {
  data() {
    return {
      event: {
        id: 1,
        title: 'Beach Cleanup',
        date: 'Tues Aug 19, 2018',
        time: '6:00',
        attendees: [
          { id: 'abc123', name: 'Adam Jahr' },
          { id: 'def', name: 'Stephane Liu' }
        ]
      }
    }
  }
}
</script>

<style scoped>
.event-card {
  padding: 20px;
  margin-bottom: 24px;
  transition: all 0.2s linear;
  cursor: pointer;
}
.event-card:hover {
  transform: scale(1.01);
  box-shadow: 0 3px 12px 0 rgba(0, 0, 0, 0.2), 0 1px 15px 0 rgba(0, 0, 0, 0.19);
}
.event-card > .title {
  margin: 0;
}

.event-link {
  color: black;
  text-decoration: none;
  font-weight: 100;
}
</style>
