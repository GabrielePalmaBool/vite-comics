<script>
import HeaderMy from './components/HeaderMy.vue'
import ListFunctions from './components/ListFunctions.vue'
export default {

  components: {
    HeaderMy,
    ListFunctions
  }

}


</script>

<template>
  <header>
    <HeaderMy />
  </header>
  <main>
    <ListFunctions />
  </main>
</template>

<style lang="scss">
@use './styles/partials/variables' as *;
@use './styles/general.scss' as *;

h4 {
  color: $primary;
}
</style>
