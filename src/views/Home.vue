<template>
  <div class="home">
    <MainPageTop></MainPageTop>
    <AboutMb></AboutMb>
    <AboutMb></AboutMb>
    <MbSelect></MbSelect>
    <Footer></Footer>
  </div>
</template>

<script>
// @ is an alias to /src
import MainPageTop from '../components/MainPageTop'
import AboutMb from '../components/AboutMB'
import MbSelect from '../components/MbSelect'
import Footer from '../components/Footer'

export default {
  name: 'Home',
  components: {
    MainPageTop,
    AboutMb,
    MbSelect,
    Footer
  }
}
</script>
