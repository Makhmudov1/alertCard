<script setup>
import AlertCard from './components/alertCard.vue'


const alerts = [
    {
        'text': 'По заказу 509/1718223677 выставлен счет.',
        'date': '18 января',
        'time': '14:26',
        'href': '#',
        'isReady': false
    },
    {
        'text': 'По заказу 509/1718223677 выставлен счет.',
        'date': '18 января',
        'time': '14:26',
        'href': '#',
        'isReady': false
    },
    {
        'text': 'По заказу 509/1718223677 выставлен счет.',
        'date': '18 января',
        'time': '14:26',
        'href': '#',
        'isReady': true
    },
    {
        'text': 'По заказу 509/1718223677 выставлен счет.',
        'date': '18 января',
        'time': '14:26',
        'href': '#',
        'isReady': true
    },
    {
        'text': 'По заказу 509/1718223677 выставлен счет.',
        'date': '18 января',
        'time': '14:26',
        'href': '#',
        'isReady': true
    },
    {
        'text': 'По заказу 509/1718223677 выставлен счет.',
        'date': '18 января',
        'time': '14:26',
        'href': '#',
        'isReady': true
    },
    {
        'text': 'По заказу 509/1718223677 выставлен счет.',
        'date': '18 января',
        'time': '14:26',
        'href': '#',
        'isReady': true
    },
    {
        'text': 'По заказу 509/1718223677 выставлен счет.',
        'date': '18 января',
        'time': '14:26',
        'href': '#',
        'isReady': true
    },
]
</script>

<template>
  <div class="container max-w-4xl font-segoe">
      <AlertCard v-for="(alert, index) in alerts" :key="index" :item="alert"/>
  </div>
</template>

<style scoped>

</style>
