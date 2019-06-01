<template>
  <div class="container fill-height">
    <div class="layout row wrap">
      <div class="flex xs12 md6">
        <div class="package package-wrapper">
          <img src="@/assets/img/oekotex_de.png" class="package-logo" />
          <div class="package-slider">
            <img src="@/assets/img/lillydoo-testpaket-10.jpg" />
          </div>
        </div>
      </div>
      <div class="spacer" />
      <div class="flex xs12 md5">
        <div class="package package-description">
          <h2 class="title">Unser gratis Testpaket</h2>
          <p class="subheading">Wähle Deine Größe</p>
          <div class="layout row wrap">
            <div class="package-button active">
              <p>1</p>
              <span>(2-3 KG)</span>
            </div>
            <div class="package-button">
              <p>2</p>
              <span>(3-4 KG)</span>
            </div>
            <div class="package-button">
              <p>3</p>
              <span>(4-7 KG)</span>
            </div>
            <div class="package-button">
              <p>4</p>
              <span>(7-10 KG)</span>
            </div>
            <div class="package-button">
              <p>5</p>
              <span>(10-12 KG)</span>
            </div>
          </div>
          <p>Teste jetzt unsere Windeln und Feuchttücher - In Größe 1 - 3 enthält unser Testpaket unsere Feuchttücher mit 99 % Wasser, ab Gr. 4 erhältst Du unsere Sensitiven Feuchttücher. Wir zahlen die Produkte, Du nur den Versand.</p>
          <ul class="product-list">
            <li class="primary-color">Automatischer Übergang ins jederzeit kündbare Windel-Abo für 49,50&nbsp;€ pro Lieferung.</li>
            <li>Preise inkl. MwSt., ggf. zzgl. <a href="" class="primary-color">Versandkosten</a></li>
          </ul>
          <button class="order-btn">In den Warenkorb legen</button>
        </div>
      </div>
    </div>
    <div class="layout row wrap composition">
      <div class="flex xs12">
        <h2 class="title">Dein Testpaket enthält</h2>
      </div>
      <div class="flex xs12 md6">
        <div class="layout row">
          <div class="trial-img">
            <img src="@/assets/img/preview.jpg" />
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
            <img src="@/assets/img/water-wipes-15-small.jpg" />
          </div>
          <div class="trial-info">
            <h4>15 Feuchttücher mit 99 % Wasser</h4>
            <ul>
              <li>0 % Parfüme &amp; PEGs, 100 % biologisch abbaubar</li>
              <li>Natürlich rein, extra mild, Alternative zu "Wasser &amp; Watte"</li>
            </ul>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script lang="ts">
import { Component, Vue } from 'vue-property-decorator'

@Component({
  layout: 'app',
  components: {}
})
export default class Index extends Vue {}
</script>
