<template>
  <div class="flex xs12 md5">
    <div class="package package-description">
      <h2 class="title">Unser gratis Testpaket</h2>
      <p class="subheading">Wähle Deine Größe</p>
      <div class="layout row wrap">
        <div
          v-for="{ id, weight, preview } in packages"
          :key="id"
          class="package-button"
          :class="selectedPackage.id === id ? 'active' : ''"
          @click="$emit('setPackage', { id, weight, preview })"
        >
          <p>{{ id }}</p>
          <span>{{ weight }}</span>
        </div>
      </div>
      <p>
        Teste jetzt unsere Windeln und Feuchttücher - In Größe 1 - 3 enthält
        unser Testpaket unsere Feuchttücher mit 99 % Wasser, ab Gr. 4 erhältst
        Du unsere Sensitiven Feuchttücher. Wir zahlen die Produkte, Du nur den
        Versand.
      </p>
      <ul class="product-list">
        <li class="primary-color">
          Automatischer Übergang ins jederzeit kündbare Windel-Abo für
          49,50&nbsp;€ pro Lieferung.
        </li>
        <li>
          Preise inkl. MwSt., ggf. zzgl.
          <a href="" class="primary-color">Versandkosten</a>
        </li>
      </ul>
      <button class="order-btn">In den Warenkorb legen</button>
    </div>
  </div>
</template>
<script lang="ts">
import { Component, Vue, Model } from 'vue-property-decorator'
import { Package } from '@/types'

@Component
export default class PackageSelector extends Vue {
  @Model('setPackage') selectedPackage!: Package
  packages: Package[] = [
    {
      id: 1,
      weight: '(2-3 KG)',
      preview: 'package-1'
    },
    {
      id: 2,
      weight: '(3-4 KG)',
      preview: 'package-2'
    },
    {
      id: 3,
      weight: '(4-7 KG)',
      preview: 'package-3'
    },
    {
      id: 4,
      weight: '(7-10 KG)',
      preview: 'package-4'
    },
    {
      id: 5,
      weight: '(10-12 KG)',
      preview: 'package-5'
    }
  ]
  created() {
    this.$emit('setPackage', this.packages[0])
  }
}
</script>
