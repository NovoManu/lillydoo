<template>
  <div class="layout row wrap composition">
    <div class="flex xs12">
      <h2 class="title">Dein Testpaket enthält</h2>
    </div>
    <div class="flex xs12 md6">
      <div class="layout row">
        <div class="trial-img">
          <img src="@/assets/img/preview.jpg" alt="" />
        </div>
        <div class="trial-info">
          <h4>10 Lillydoo Windeln</h4>
          <ul>
            <li>0 % Parfüme &amp; Lotionen, 100 % LILLYDOO Schutz</li>
            <li>Extra weich und mit idealer Passform</li>
          </ul>
        </div>
      </div>
    </div>
    <div class="flex xs12 md6">
      <div class="layout row">
        <div class="trial-img">
          <img :src="package.image" alt="Overview Image" />
        </div>
        <div class="trial-info">
          <h4>{{ package.title }}</h4>
          <ul>
            <li v-for="(line, index) in package.description" :key="index">
              {{ line }}
            </li>
          </ul>
        </div>
      </div>
    </div>
  </div>
</template>
<script lang="ts">
import { Component, Vue, Prop } from 'vue-property-decorator'
import { OverviewPackage } from '@/types'

@Component
export default class PackageOverview extends Vue {
  @Prop({ required: true }) package!: OverviewPackage
}
</script>
