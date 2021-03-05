
<template>
  <div id="app">
     <section class="hero is-warning is-bold is-fullheight">
        <div class="container has-text-centered">
          <ToDoCard/>

      </div>

    </section>
  </div>
</template>

<script>

import ToDoCard from '@/components/ToDoCard';

export default {
  name: 'app',
  components: {
    ToDoCard,

  },
}
</script>

<style>
.has-text-centered {
  display: flex;
  justify-content: center;
  align-items: center;

}
</style>