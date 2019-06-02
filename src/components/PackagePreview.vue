<template>
  <div class="flex xs12 md6">
    <div class="package package-wrapper">
      <img
        src="@/assets/img/oekotex_de.png"
        alt="Package Logo"
        class="package-logo"
      />
      <div class="package-slider">
        <img :src="compilePreview" alt="Package Image" />
      </div>
    </div>
  </div>
</template>
<script lang="ts">
import { Component, Prop, Vue } from 'vue-property-decorator'

@Component
export default class PackagePreview extends Vue {
  @Prop({ required: false }) preview!: string
  get compilePreview(): string {
    return this.preview
      ? require(`@/assets/img/${this.preview}.jpg`)
      : require('@/assets/img/package-1.jpg')
  }
}
</script>
