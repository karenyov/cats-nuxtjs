<!-- HomePage.vue -->
<template>
  <div class="page-base">
    <h1>Cats API</h1>
    <b-row>
      <b-col md="4" v-for="item in items" :key="item.id">
        <Card
          :name="item.name"
          :image="item.reference_image_id"
          :description="item.description"
        />
      </b-col>
    </b-row>
  </div>
</template>

<script>
import Card from '@/components/Card.vue';
import axios from 'axios';

export default {
  name: 'HomePage',
  layout: 'DefaultLayout',
  components: {
    Card
  },
  data() {
    return {
      items: []
    };
  },
  async asyncData({ $axios }) {
    const items = await $axios.$get('https://api.thecatapi.com/v1/breeds')
    return { items }
  }
}
</script>

<style>
  .page-base {
    display: flex;
    justify-content: center;
    flex-direction: column;
    align-items: center;
    padding: 50px;
  }
</style>
