<template>
  <section id="FacebookComment">
    <div id="fb-root"></div>
    <div class="fb-comments"></div>
  </section>
</template>

<script>
import { facebookAppId } from '@/config'

export default {
  name: 'FacebookComment',
  mounted () {
    (function (d, s, id) {
      var js
      var fjs = d.getElementsByTagName(s)[0]
      if (d.getElementById(id)) return
      js = d.createElement(s); js.id = id
      js.src = `https://connect.facebook.net/en_GB/sdk.js#xfbml=1&version=v3.0&appId=${facebookAppId}&autoLogAppEvents=1`
      fjs.parentNode.insertBefore(js, fjs)
    }(document, 'script', 'facebook-jssdk'))
  }
}
</script>
