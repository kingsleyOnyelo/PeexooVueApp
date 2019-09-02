<template>
  <FullCalendar defaultView="dayGridMonth" :plugins="calendarPlugins"  
  :events="events"
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
      calendarPlugins: [ dayGridPlugin ],
      events : [
            { title: 'event 4', date: '2019-09-02' },
            { title: 'event 1', start: '2019-09-09',  end: '2019-09-12'  }
      ]
    }
  }
}

</script>

<style lang='scss'>

@import '~@fullcalendar/core/main.css';
@import '~@fullcalendar/daygrid/main.css';

</style>