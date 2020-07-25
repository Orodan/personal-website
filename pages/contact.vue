<template>
  <section class="contact">
    <section class="left">
      <img src="~/assets/tiny-rick.jpg" alt="profile picture">
    </section>

    <section class="right">
      <ul class="labels">
        <li><strong>Mail:</strong></li>
        <li><strong>Twitter:</strong></li>
        <li><strong>Linkedin:</strong></li>
        <li><strong>Github:</strong></li>
      </ul>
      <ul class="values">
        <li><span>john.doe@gmail.com</span></li>
        <li><span>Orodan</span></li>
        <li><span>Jimmy Kasprak</span></li>
        <li><span>Oroden</span></li>
      </ul>
    </section>

  </section>
</template>

<script>
export default {
  data () {
    return {
      title: 'Jimmy Kasprzak | contact',
    }
  },
  head () {
    return {
      title: this.title,
    }
  }
}
</script>

<style scoped>
.contact {
  padding: 100px 40px;
  display: flex;
  background: linear-gradient(120deg, var(--white) 50%, var(--red) 50%);
}

.left {
  flex: 1;
  display: flex;
  justify-content: center;
  align-items: center;
}

.right {
  flex: 1;
  display: flex;
  justify-content: center;
  align-items: center;
  color: var(--white);
}

.right > * {
  flex: 1;
}

ul {
  list-style: none;
  padding: 0;
}

li {
  width: 100%;
  padding: 10px;
}

.labels li {
  text-align: left;
  padding-left: 50%;
}

.values li {
  text-align: left;
}

.right > div:first-child strong {
  text-align: left;
}

strong, span {
  padding: 10px;
  font-size: 18px;
}

img {
  width: 200px;
  height: 200px;
  border-radius: 50%;
}
</style>
