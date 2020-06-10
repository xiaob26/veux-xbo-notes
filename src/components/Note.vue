<template>
  <div class ='item'>
      <div class= 'xbo'>
      {{updated(entity)}} 
      </div>

      <div class="content">
        <div class= 'header' @click="open = !open">
        {{header(entity) || '新建笔记'}}
        
          
        </div>
        <div class ='extra'>
          <editor :entity='entity' v-if="open"></editor>
           {{words(entity)}} 字
        <i class='right floated trash outline icon'
        @click="destroy(entity)"
        v-if="open"
        > </i>
        </div>
      </div>
    </div>
</template>

<script>
import Editor from './Editor'
import {mapGetters,mapActions} from 'vuex'
export default {
    name: 'Note',
    components: {
        Editor
    },
    props: [
      'entity'
    ],
    computed: {
      ...mapGetters([
        'updated',
        'words',
        'header'
      ])
    },
    methods: {
      ...mapActions([
        'destroy'
      ])
    },
    data () {
      return {
        open:false
      }
    }
     
    

}
</script>

<style>
.xbo{
  margin-right: 10px;
}

</style>