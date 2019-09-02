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
            { title: `Mrs Steven daughter's wedding photography`, date: '2019-09-02' },
            { title: `Mrs Peter daughter's wedding photography`, start: '2019-09-09',  end: '2019-09-12'  }
      ]
    }
  }
}

</script>

<style lang='scss'>

@import '~@fullcalendar/core/main.css';
@import '~@fullcalendar/daygrid/main.css';

.fc-event {
    position: relative;
    display: block;
    font-size: 0.85em;
    line-height: 1.4;
    border-radius: 3px;
    border: 1px solid #ffb500;
}
.fc-event, .fc-event-dot {
    background-color: #ffc107;
}
span.fc-title{
    white-space: pre-wrap;
    color: #fff;
    text-align: center;
    display: block;
    padding: 10px;
}
.fc-unthemed td.fc-today{
    background-color: #FFF3D4;
}
</style>