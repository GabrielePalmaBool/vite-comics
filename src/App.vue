<script>
import Header from './components/Header.vue'

export default {

  components: {
    Header
  }

}


</script>

<template>
  <Header />
</template>

<style lang="scss">
@use './styles/partials/variables' as *;
@use './styles/general.scss' as *;

h4 {
  color: $primary;
}
</style>
