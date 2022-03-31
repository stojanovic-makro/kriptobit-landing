<template>
  <div style="position: relative">
    <div class="rectangle-gradient" />
    <div class="wrapper" style="margin: 0 auto">
      <div class="small-title">
        Small Title
      </div>
      <h1>H1 - Heading</h1>
      <h2>H2 - Heading</h2>
      <h3>H3 - Sub heading</h3>
      <p class="t1">T 1 - Text</p>
      <p class="t1">Commodo imperdiet ut parturient arcu sed. Enim, massa amet duis consectetur odio faucibus. Hendrerit commodo pellentesque diam eu et facilisi adipiscing.</p>
      <p class="t2">T 2 - Small text</p>
      <p class="t2">Commodo imperdiet ut parturient arcu sed. Enim, massa amet duis consectetur odio faucibus. Hendrerit commodo pellentesque diam eu et facilisi adipiscing.</p>
      <div class="header-light">Menu Links</div>
      <div class="row" style="gap: 48px">
        <Button label="PRIJAVI SE" />
        <Button color="bg-brand" label="PRIJAVI SE" />
      </div>
    </div>
  </div>
</template>

<script>
import Button from '~/components/ui/Button'

export default {
  name: 'TestPage',
  components: { Button },
}
</script>