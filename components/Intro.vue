<template>
  <section class="intro">
    <slot></slot>
  </section>
</template>

<style>
.intro {
  padding: 60px 40px;
  font-size: 26px;
}

@media only screen and (max-width: 768px) {
  .intro {
    font-size: 24px;
  }
}
</style>
