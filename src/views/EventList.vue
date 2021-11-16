<template>
<h1>Evenciki</h1>
  <div class="events">
    <EventCard v-for="event in events" :key="event.id" :event="event"/>
  </div>
</template>

<script>
// @ is an alias to /src
import EventCard from "@/components/EventCard.vue";

export default {
  name: "Home",
  components: {
    EventCard,
  },
  data(){
    return{
      events:[
      {
        id: 48922023,
        category: 'weddings',
        title: 'Pakistanian Walima Wedding',
        description: 'Invitation for the most colorful wedding of the year',
        location: 'Karachi',
        date: 'January 23, 2022',
        time: '18:00',
        petsAllowed: true,
        organizer: 'Alibaba'
      },
      {
        id: 48922024,
        category: 'coming back',
        title: 'Welcome Janko in home',
        description: 'Janko finally will be at home',
        location: 'Warsaw',
        date: 'November 19, 2021',
        time: '19:00',
        petsAllowed: false,
        organizer: 'Koza'
      },
      {
        id: 48922025,
        category: 'meetings',
        title: 'Turban day',
        description: 'Bring with yourself turban and goat',
        location: 'Somewhere in the forest',
        date: 'Decmeber 09, 2021',
        time: '11:00',
        petsAllowed: true,
        organizer: 'Turbanierzy'
      },]
    }
  }
};
</script>

<style scoped>
.events {
  display: flex;
  flex-direction: column;
  align-items: center;
}
</style>
