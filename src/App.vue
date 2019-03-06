<template>
  <div>
    <vending-machine></vending-machine>
    <drink></drink>
  </div>
</template>

<script>

import VendingMachine from './components/VendingMachine'
import Drink from './components/Drink'
export default {
  name: 'App',
  components: {
    VendingMachine,
    Drink
  }
}
</script>

<style>

</style>
