<template>
  <div class="calendar-header">
      <calendar-move-button icon="keyboard_arrow_left"></calendar-move-button>
      <calendar-header-text-detail></calendar-header-text-detail>
      <calendar-move-button icon="keyboard_arrow_right"></calendar-move-button>
  </div>
</template>

<script lang="ts">
import { Vue , Component } from "vue-property-decorator";
import CalendarMoveButton from "./CalendarMoveButton.vue";
import CalendarHeaderTextDetail from "./CalendarHeaderTextDetail.vue";
@Component({
    components : {
        CalendarMoveButton,
        CalendarHeaderTextDetail
    }
})
export default class CalendarHeaderNavigator extends Vue {

}
</script>

<style lang="scss" scoped>
.calendar-header {
    display:flex;
    align-items: center;
    justify-content: space-between;
    padding: 0 5%;
}
</style>