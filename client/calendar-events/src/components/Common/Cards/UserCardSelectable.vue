<template>
  <card-flat class="user-card">
    <div class="avatar">
      <avatar-image variant="featured" :src="image" />
    </div>
    <div class="detail">
      <div class="detail__content">
        <text-label fontSizeText="normal" :weight="true" class="title">{{title}}</text-label>
        <text-label variant="smooth" fontSizeText="small">{{detail}}</text-label>
      </div>
      <div class="detail__extra">
        <slot></slot>
      </div>
    </div>
  </card-flat>
</template>

<script lang="ts">
import { Component, Prop, Vue } from "vue-property-decorator";
import { AvatarImage } from "@/components/Common/AvatarImages";
import { TextLabel } from "@/components/Common/TextLabels";
import { CardFlat } from '.';

@Component({
  components: {
    AvatarImage,
    TextLabel,
    CardFlat
  },
})
export default class UserCardSelectable extends Vue {
  @Prop() image !: string;
  @Prop() title !: string;
  @Prop() detail !: string;
}
</script>

<style lang="scss" scoped>
.user-card {
  display: flex;
  padding: 15px;
  align-items: center;
  box-shadow: 0 10px 30px rgba(0,0,0,.03);
  .avatar {
    margin-right: 6px;
  }
  .detail {
    &__content {
      display: flex;
      flex-direction: column;
      .title {
        margin-bottom: 4px;
      }
    }
  }
}
</style>
