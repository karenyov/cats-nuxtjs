<template>
<div>
  <b-card-group deck class="card-cat-row">
    <b-card :title="name" img-alt="Image" img-top class="card-cat">
      <img :src="`https://cdn2.thecatapi.com/images/${image}.jpg`" class="card-img" />
      <b-card-text>
        This is a wider card with supporting text below as a natural lead-in to additional content.
        This content is a little bit longer.
      </b-card-text>
      <template #footer>
        <small class="text-muted">Last updated 3 mins ago</small>
      </template>
    </b-card>
  </b-card-group>
</div>

</template>

<script>
export default {
  name: 'Card',
  props: {
    name: String,
    image: String,
    description: String
  }
}
</script>

<style>
  .card-cat-row {
    margin-bottom: 20px;
  }

  .card-cat {
    width: 100%;
    max-width: 250px;
    height: 400px;
  }
</style>
