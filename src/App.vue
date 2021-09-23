<template>
  <Navbar />
  <Homepage />
  <Footer />
</template>

<script>
import Homepage from './components/Homepage'
import Navbar from './components/Navbar'
import Footer from './components/Footer'

export default {
    name: 'App',
    components: {
      Homepage,
      Navbar,
      Footer
    }
}
</script>

<style>

</style>
