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
  props:{
    events:{
      type: Array,
      required: true
    }
  },
  data() {
    return {
      calendarPlugins: [ dayGridPlugin ],
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

.fc-button-primary:disabled {
    color: #ffc107;
    border-color: #ffc107;
    background: transparent;
    padding-left: 30px;
    padding-right: 30px;
}
</style>