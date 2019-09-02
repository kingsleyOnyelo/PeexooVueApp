<template>
  <FullCalendar defaultView="dayGridMonth" :plugins="calendarPlugins"  
  :events="[
  { title: 'event 4', date: '2019-09-02' },
    { title: 'event 1', date: '2019-09-09' },
    { title: 'event 2', date: '2019-09-10' },
    { title: 'event 3', date: '2019-09-11' },
  ]"
  />
</template>
<script>

import FullCalendar from '@fullcalendar/vue'
import dayGridPlugin from '@fullcalendar/daygrid'

export default {
  components: {
    FullCalendar // make the <FullCalendar> tag available
  },
  data() {
    return {
      calendarPlugins: [ dayGridPlugin ]
    }
  }
}

</script>

<style lang='scss'>

@import '~@fullcalendar/core/main.css';
@import '~@fullcalendar/daygrid/main.css';

</style>