<template>
    <div>
    <Main/>
    <Spec/>
        <Stack/>
        <City/>
        <Do/>
        <Contact/>
    </div>
</template>

<script>
import Main from './components/Main.vue'
import Spec from './components/Spec'
import Stack from './components/Stack'
import City from './components/City'
import Do from './components/Do'
import Contact from './components/Contact'
export default {
  name: 'App',
  components: {
      Main,
      Spec,
      Stack,
      City,
      Do,
      Contact
  }
}
</script>

<style>

</style>
