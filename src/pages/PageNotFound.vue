<template>
  <div class="col-full" :class="$style.centered">
    <h1 :class="$style.headingLarge">Not Found</h1>
    <p :class="$style.textLarge">And I stillll haven't found what I'm looking for.</p>
    <p :class="$style.textLarge"><router-link :to="{name: 'PageHome'}">Go Home and Try Again</router-link></p>
  </div>
</template>

<script>

export default {

}
</script>

<style module>
.headingLarge {
  font-size: 80px;
}
.textLarge {
  font-size: 40px;
  font-weight: 100;
}
div {
  text-align: center;
}

</style>