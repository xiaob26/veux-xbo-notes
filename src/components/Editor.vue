<template>
  <div class= 'ui form' >
    <div class = 'field'>
      <textarea  rows="5"
      placeholder='开始记录点东西吧...'
      v-model="entity.body" 
      @input="update(entity)"
       >
      </textarea>

    </div>

  </div>
</template>

<script>
import {mapActions} from 'vuex'
export default {

  props: [
      'entity'
  ],
  methods: {
    ...mapActions([
      'update'
    ])
  }
}
</script>

<style>

</style>