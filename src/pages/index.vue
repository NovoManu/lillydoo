<template>
  <div class="container fill-height">
    <div class="layout row wrap">
      <PackagePreview :preview="selectedPackage.preview" />
      <div class="spacer" />
      <PackageSelector v-model="selectedPackage" />
    </div>
    <PackageOverview :package="overviewPackage" />
  </div>
</template>
<script lang="ts">
import { Component, Vue } from 'vue-property-decorator'
import { Package, OverviewPackage } from '@/types'
import PackagePreview from '@/components/PackagePreview.vue'
import PackageSelector from '@/components/PackageSelector.vue'
import PackageOverview from '@/components/PackageOverview.vue'

@Component({
  layout: 'app',
  components: {
    PackagePreview,
    PackageSelector,
    PackageOverview
  }
})
export default class Index extends Vue {
  selectedPackage: Package | {} = {}
  get overviewPackage(): OverviewPackage {
    const packages: OverviewPackage[] = [
      {
        image: require('@/assets/img/overview-1.jpg'),
        title: '15 FEUCHTTÜCHER MIT 99 % WASSER',
        description: [
          '0 % Parfüme & PEGs, 100 % biologisch abbaubar',
          'Natürlich rein, extra mild, Alternative zu "Wasser & Watte"'
        ]
      },
      {
        image: require('@/assets/img/overview-2.jpg'),
        title: '15 SENSITIVE FEUCHTTÜCHER',
        description: [
          '0 % Parfüme & PEGs, 100 % biologisch abbaubar',
          'Extra dickes und kompostierbares Tuch'
        ]
      }
    ]
    return (this.selectedPackage as Package).id < 4 ? packages[0] : packages[1]
  }
}
</script>
