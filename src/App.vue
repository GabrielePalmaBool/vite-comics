<script>
import HeaderMy from './components/HeaderMy.vue'
import ListFunctions from './components/ListFunctions.vue'
import FooterMy from './components/FooterMy.vue'

export default {

  components: {
    HeaderMy,
    ListFunctions,
    FooterMy
  }

}
</script>

<template>
  <HeaderMy />
  <ListFunctions />
  <FooterMy />
</template>

<style lang="scss">
@use './styles/partials/variables' as *;
@use './styles/general.scss' as *;

h4 {
  color: $primary;
}
</style>
